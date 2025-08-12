---
layout: default
title: Step 2 - Prep and QC Your Data
parent: Full Archive Workflow
nav_order: 2
---

# Step 2: Prep and QC Your Data

This step involves organizing, cleaning, and performing quality control checks on your data to ensure it is accurate, consistent, and well-documented before moving forward.

---

## Stage 1: Organize & Clean Your Data


### Describe and Preserve Your Data
* **Backup Raw Data:** Always save a copy of the untouched, raw data in a separate, secure location as a backup.
* **Document Changes:** Keep a log or script of all changes you make to your data during the cleaning process. This is crucial for reproducibility.
* **Understand Requirements:** Be aware of when and where your data will need to be submitted for long-term storage.

### Create a Consistent File Structure
* **Organize Folders:** Use a logical folder structure to easily locate raw data, processed data, scripts, and final outputs.
* **Use Standard Naming Conventions:**
    * **No Special Characters:** Avoid `!`, `@`, `#`, `$`, `%`, etc. in filenames.
    * **No Spaces:** Use underscores `_` or hyphens `-` instead of spaces (e.g., `Raw_Data_2022.csv`).
    * **Be Descriptive:** Name files in a way that you'll understand in the future.
    * **Be Consistent:** Use the same case (e.g., `UPPERCASE`, `lowercase`, `CamelCase`) for all your files.

### Clean Your Data Columns
* **One Data Type per Column:** Ensure each column contains only one type of data (e.g., all numbers, all text, or all dates).
* **Separate Units from Data:** Keep units in the column header (e.g., `Depth_Meters`) and the data as numbers (e.g., `10`), not `10m`.
* **Check for Uniqueness:** If you have a `UNIQUE_ID` column, verify that every ID is truly unique.
* **Check for Typos:** For text columns, create a sorted list of all unique values to easily spot and correct misspellings or inconsistent entries (e.g., "USA" vs "U.S.A.").
* **Define Nulls:** Be clear about what empty cells mean. Define in your data dictionary whether a blank cell means `0`, `NA`, or something else.

---

## Stage 2: Perform Data Integrity & QC Checks

Once the data is organized, perform these specific quality control checks on the data itself.

### Verify Standard Metadata Fields
Ensure all standard descriptive fields are included for every record to describe the "where, when, who, and what" of the data.

<details>
<summary>Click to see all required metadata fields</summary>
  <ul>
    <li>Mission</li>
    <li>Region/Island</li>
    <li>Site</li>
    <li>Latitude/Longitude</li>
    <li>Depth</li>
    <li>Date (and time if relevant - preferred format `YYYY-MM-DD`)</li>
    <li>Diver</li>
    <li>Method/Instrument type</li>
  </ul>
</details>

### Check for Accuracy and Consistency
* **Check for Unexpected Missing Values:** Look for empty cells in columns where data should always be present, such as `Latitude/Longitude`, `Site`, `Depth`, etc.
* **Check the Range of Values:** Look for outliers. Does the range of values make sense for the location and metric? (e.g., `Depth > 30m?`, `a fish length of 1000cm?`).
* **Check for Consistency:** Do all `SITE_ID`s follow the same format? Are there any codes used that don't apply to the dataset?

### Verify Method-Specific Rules
Ensure the data follows all rules required by the scientific collection method.

<details>
<summary>Click to see examples of method rules</summary>
  <ul>
    <li><strong>Required Value:</strong> e.g., `RECENT DEAD %` must be a value between 0–100.</li>
    <li><strong>If/Then Logic:</strong> e.g., If `CONDITION` is "Bleaching," then the `SEVERITY` column must have a value.</li>
    <li><strong>Formula Check:</strong> e.g., `OLD_DEAD` + `RECENT_DEAD` must be ≤ 100%.</li>
    <li><strong>Constraint:</strong> e.g., `LENGTH` must be ≥ 5 cm for adult coral surveys.</li>
    <li><strong>Exception:</strong> e.g., If `LENGTH` is < 5 cm, is the colony type listed as a `FRAGMENT`?</li>
  </ul>
</details>

---


## Helpful Tools

* [Folder Stats Tool]({{ '/docs/Folder-Stats-Tool.html' | relative_url }})
* [File Copy Tool]({{ '/docs/File-Copy-Tool.html' | relative_url }})
* [Archive Manifest File Tool]({{ '/docs/Archive-Manifest-File-Tool.html' | relative_url }})
* [Clear Thumbs Database Tool]({{ '/docs/Clear-Thumbs-Database-Tool.html' | relative_url }})
* [Garmin GPS File Converter Tool]({{ '/docs/Garmin-GPS-File-Converter.html' | relative_url }})
* [Heic Heif Converter Tool]({{ '/docs/Heic-Heif-Converter-Tool.html' | relative_url }})


---
<a href="{{ '/docs/Step-3-Register-Data-in-InPort.html' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Next Step: Register Your Data in InPort
</a>

