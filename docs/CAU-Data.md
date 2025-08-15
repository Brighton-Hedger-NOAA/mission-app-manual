---
layout: default
title: Folder Stats Tool
parent: Archiving Tools
nav_order: 1
---
## Folder Stats Tool

The Folder Stats Tool scans a selected directory and creates a CSV file that reports the size of each subfolder. It’s a quick way to estimate archive size or prep data for cloud upload.

---

### When It's Useful

- Estimating total data volume for archival  
- Identifying large or unexpected folders before transfer  
- Pre-checking folders prior to uploading to NODD or Google Cloud Bucket
- Helps decide which folders to copy/move/upload first  

---

### How to Use It

1. Download the [folderstatstool.exe](https://Brighton-Hedger-NOAA.github.io/data-archiving-guide/tools/folderstatstool.exe)
2. Double click the program to run (if needed right-click the file → **Properties** → Check **Unblock**)
   <img width="320" height="400" alt="image" src="https://github.com/user-attachments/assets/fc2b8454-eda8-49ab-bdf1-f6a1f6614c81" />
3. Click **Browse** and select the folder you want to scan

   <img width="360" height="315" alt="image" src="https://github.com/user-attachments/assets/769cbe91-1cf6-4643-83f2-cb91b40b1b40" /><img width="458" height="325" alt="image" src="https://github.com/user-attachments/assets/886ca35e-b68a-4faf-8451-624cb88858c5" />
4. Click **Start**
5. Wait for the tool to finish scanning — a status message will appear

   <img width="360" height="310315" alt="image" src="https://github.com/user-attachments/assets/fb74df27-609c-4f1c-aae6-632c656401b2" /><img width="360" height="315" alt="image" src="https://github.com/user-attachments/assets/95434f10-1fa0-4be1-97a8-a3fb97a5000f" />



---

### Output

- A `.csv` file will be saved in the root of the scanned folder  
- File includes:
  - Folder path  
  - Total size
  - Scan timestamp 
- Example filename:  
  `10_12_2022_1126_folder_size_log.csv`

<img width="740" height="500" alt="image" src="https://github.com/user-attachments/assets/21057147-4e91-4e3c-b79c-e56233f96ac5" />

---

<a href="{{ '/docs/Tools' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Back to All Tools
   
<a href="{{ '/docs/Step-3-Register-Data-in-InPort' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Next Step: Register Your Data in InPort
