---
layout: default
title: 'Special Cases: Imagery & Code'
nav_order: 4
---

# Special Cases: Imagery & Code

While the main workflow covers standard tabular data, some data types like code scripts or very large imagery sets have a specialized archiving process.

<style>
  .special-case-tabs {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 2px solid #ccc;
    margin-top: 2rem;
    font-family: sans-serif;
  }

  .sc-tab {
    padding: 0.5rem 1rem;
    margin-right: 0.25rem;
    background-color: #f0f0f0;
    border: 1px solid #ccc;
    border-bottom: none;
    border-radius: 4px 4px 0 0;
    font-weight: bold;
    font-size: 0.9rem;
    color: #003366;
    cursor: pointer;
  }

  .sc-tab.active {
    background-color: #ffffff;
    border-bottom: 2px solid white;
    position: relative;
    top: 1px;
  }

  .sc-tab-content {
    display: none;
    padding: 1rem;
    border: 1px solid #ccc;
    border-top: none;
    font-family: sans-serif;
  }

  .sc-tab-content.active {
    display: block;
  }
</style>

<div class="special-case-tabs">
  <div class="sc-tab active" onclick="showTab('imagery')">Imagery</div>
  <div class="sc-tab" onclick="showTab('code')">Code/Scripts</div>
</div>

<div id="imagery" class="sc-tab-content active" markdown="1">
## Archiving Large Datasets or Imagery (NODD Workflow)

For very large datasets or imagery collections that are handled by the NOAA Open Data Dissemination (NODD) system, follow this workflow. If you have never used google cloud before or done anything with NODD, click [here](/data-archiving-guide/docs/NODD-set-up) for a NODD set up guide!

### Action Items

- [ ] Refer to the **[NODD Set Up Guide](/data-archiving-guide/docs/NODD-set-up)** if you do not have access to the Google Cloud Bucket, do not have GoogleSDK installed, or have never initialized the gloud CLI steps

- [ ] **Prepare Data:** If syncing folders, organize your local data directory structure and identify any extraneous file types or unnecessary data.
> If syncing files, create list of files for upload. Sample [here](https://docs.google.com/spreadsheets/d/1P0EV1LwER8NLgafMUStDUtVweqfiR7uiUOChitkOtw8/)

- [ ] **Evaluate Upload Size:** Evaluate the total size of your data and, if necessary, split it into appropriate batch sizes (e.g., less than 1TB per upload).
> Can use the [folder stats tool](/data-archiving-guide/docs/Folder-Stats-Tool) to see file and folder size quickly

- [ ] **Prepare Script:** Your have a few options for completing uploads:
    1. Use the NODD upload tool (preferred)
        - Insert the source directory in the "Copy From" box
        - Insert the Google coud Bucket destination directory in the "Copy to Path" box
        - Choose a place you want the copy log to be for the "Copy Log Path" box
        - Check 'enable_multi" and "recursive_copy"
        - For faster uploading, slide the "threads" bar to 12
        - <img width="500" height=auto alt="Example:" src="{{ '/assets/nodd_app_01.png' | relative_url }}" />
    2. Paste a similar script into the GoogleSDK Shell

        ```
        gsutil -o "GSUtil:parallel_thread_count=12" -m rsync -r -n -x "(^.*(?<!\.JPG)$)|(.*_archive.*|.*_YEAR.*|.*ISLAND.*|.*SITE-ID.*|.*SITE_PHOTOS.*|.*uncorrected.*|.*MISC.*|.*DARK.*|.*Products.*)" C:\Users\Michael.Akridge\Desktop\nodd\test gs://nmfs_odp_pifsc/PIFSC/ESD/ARP/test
        ```
        - **gsutil:** This is the command-line tool for interacting with Google Cloud Storage. https://cloud.google.com/storage/docs/gsutil
        - **-o "GSUtil:parallel_thread_count=12"** if use multi-threading, limit bandwidth usage with this flag. 12 threads is the recommendation for balanced approach.
        - **-m:** This flag enables multi-threading, which speeds up the transfer by using multiple connections.
        - **rsync**: This is the command to synchronize files and directories between a local and a remote location.
        - **-r:** This flag tells rsync to perform a recursive copy of the entire directory tree.
        - **-n:** This flag performs a "dry run," which means that the synchronization will be simulated, and no actual data will be transferred. This is useful to preview what would happen if the command were executed without actually making any changes.
          - **-x:** This flag excludes files and directories that match any of the specified patterns using regular expressions.
              - The **-x** excluded patterns in detail in this case are:

              >  `(^.*(?<!\.JPG)$)` — Matches any files that do not end with the ".JPG" extension.

              >  `(.*_archive.*|.*_YEAR.*|.*ISLAND.*|.*SITE-ID.*|.*SITE_PHOTOS.*|.*uncorrected.*|.*MISC.*|.*DARK.*|.*Products.*)` — Matches any files or directories that contain any of the specified strings.
        - **local_dir** C:\Users\Michael.Akridge\Desktop\nodd\test: This is the local directory that will be synchronized.
        - **cloud_dir** gs://nmfs_odp_pifsc/PIFSC/ESD/ARP/test: This is the Google Cloud Storage bucket and destination path where the data will be synchronized.


- [ ] **Verify Upload:** After the process completes, verify the size of the upload using the command `gsutil du -sh gs://your-bucket-name/path/to/remote/directory/`. You can also re-run the `rsync` command to confirm all files were completed.

- [ ] **Tips:**
    - *Schedule Upload:* To avoid bandwidth issues, schedule large uploads for off-peak hours (after 4pm or on weekends). A 1TB upload can take approximately 24 hours.
    - *Prepare Laptop:* For the upload, connect your computer via an IRC network cable (do NOT use VPN for large transfers).

</div>

<div id="code" class="sc-tab-content" markdown="1">
## Archiving Code (R Scripts, etc.)

R scripts are not archived with NCEI but are required to be publicly accessible to comply with the PARR memorandum and FAIR data principles (Findability, Accessibility, Interoperability, and Reusability). The goal is to make your code both human- and machine-readable. Code should be accessible internally on the PIFSC GitLab and externally on GitHub.

### Action Items

- [ ] **Get set up on GitLab and GitHub.** You will need an internal PIFSC GitLab account for your workspace and version control, as well as an external GitHub repository linked to your personal work email.
    - Your NOAA GitHub account must use your NOAA email, have a profile photo, and use two-factor authentication. It is good practice for the username to be in the format `FirstLast-NOAA`.
- [ ] **Ensure your repository meets all NOAA requirements.** Repositories must give write access only to NOAA users, include a specific disclaimer in the README file, include specific wording in the LICENSE file, and have a "gold standard" backup.
- [ ] **Create a comprehensive README file.** This document should include plain text instructions, descriptions of folders and files, a software license that informs users how they may or may not use the software, and instructions on how to cite the work.
- [ ] **Link the GitHub repository in your data's metadata.** The link to the external GitHub repository must be provided as a 'URL' on the InPort metadata record and under 'References' on the S2N stub.
</div>


<script>
  function showTab(tabId) {
    document.querySelectorAll('.sc-tab-content').forEach(tab => {
      tab.classList.remove('active');
    });
    document.querySelectorAll('.sc-tab').forEach(tab => {
      tab.classList.remove('active');
    });
    document.getElementById(tabId).classList.add('active');
    event.target.classList.add('active');
  }
</script>
