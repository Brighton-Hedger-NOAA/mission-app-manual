---
layout: default
title: NODD Set Up Guide
nav_order: 1
parent: Special Cases Like Imagery and Code
---

# NODD Set Up Guide

## NODD (NOAA Open Data Dissemination) is the Workflow we use to archive large datasets, like imagery, it requires several set up steps before beginning.

---

## Action Items

- [ ] Request access to the [Google Cloud Bucket](https://console.cloud.google.com/storage/browser/nmfs_odp_pifsc;tab=objects?inv=1&invt=Ab4n9A&project=nmfs-trusted-images&pageState=(%22StorageObjectListTable%22:(%22f%22:%22%255B%255D%22))&prefix=&forceOnObjectsSortingFiltering=false) from the DST
- [ ] Submit a [JIRA](https://apps-st.fisheries.noaa.gov/jirasm/servicedesk/customer/portal/4) ticket for Google SDK to be installed
> You must fill out and attach this [Software Request Form](https://drive.google.com/file/d/1JBxrk6EBT5aot3KBiYG3CCsPNd864S6c/view?usp=drive_link)
- [ ] Once Google SDK is intalled run through and initialize the [gloud CLI steps](https://cloud.google.com/storage/docs/discover-object-storage-gsutil#before-you-begin) in the Google SDK shell
- [ ] Verify that you have Python and/or Anaconda installed
> If you do not you can still upload to gcloud using the command line script on the [NODD](/data-archiving-guide/docs/Special-Cases-Like-Imagery-and-Code) page, but you will not be able to use the *Upload Tool*
- [ ] You may need to download these Anaconda packages:
> <code> pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib rsync</code>