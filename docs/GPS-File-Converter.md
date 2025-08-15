---
layout: default
title: GPS Data Entry
parent: Data Manager
nav_order: 1
---

# GPS Data Entry


1. [GPS Download and Convert]({{ '/docs/GPS-File-Converter.html#gps-download--convert'| relative_url }})  
2. [QC the Converted GPS File]({{ '/docs/GPS-File-Converter.html#qc-the-converted-gps-file'| relative_url }})
3. [Load GPS data into Mission App]({{ '/docs/GPS-File-Converter.html#load-gps-data-into-mission-app'| relative_url }})
4. [Updating the Site Visit Table]({{ '/docs/GPS-File-Converter.html#updating-the-site-visit-table'| relative_url }})

---

1. ## **GPS Download & Convert**  
  **a)** Choose Conversion Software:  
     * Download the standalone tool ([garmin-gps-file-converter.exe]({{ '/assets/gpxconverter_windows_standalone.exe' | relative_url }}))  
      OR
     * Use the tool in the <a href="https://drive.google.com/file/u/0/d/17eXGXZ3mVWMapz2Fl9RCU27uxaOTtgJv/edit" target="_blank" rel="noopener noreferrer">cloud/online</a>  
     > You may need to request access 
       
      **b)** Using USB, connect DNR Garmin to your computer.  
      **c)** Save GPS file .gpx of that day to Cruise Folder (T drive) for specific GPS and Site type.    
      > <code> T:\Cruise\CruiseData\MP240al\GPS Downloads\Random\GPSA\ </code>  

    **d)** Use converter to convert the .gpx file to produce a .txt file in the same directory.

2. ## **QC the Converted GPS File**
* QC the .txt file produced to ensure site names are correct.  
        * Does the site name match the dive nav?  
        * If changes need to be made, update & save the .txt file.  
      
          {: .note }
          If having issues loading, try removing extra 0’s or adding in 0 E.g. TIN-0885 to TIN-885

3. ## **Load GPS data into Mission App**
  **a)** Login to the [Mission Application](https://picmidd.nmfs.local/gisd/r/gisdat/mission-app/) (if you need password reset, contact Lori/Michael)  
    > Navigate to: Home Page -> GPS Upload  

      **b)** For Fish/random sites select **REA**, For OCC/fixed sites, select **OCC** (see below)
          ![Screenshot of the Mission App GPS Upload Page]({{ '/assets/Screenshot-2025-08-13-142938.png' | relative_url }}){: width="60%" }  
      **c)** Random Site GPS Upload 
      * Select the **Team** (Fish) and **Cruise Leg**  
      * Open the text file of the GPS waypoints copy the text file & paste into the loader  
      > Make sure to copy the **header <code>(ident,lat,long,time,ltime)</code>** and the data

      * ![Screenshot of the REA GPS Entry Page]({{ '/assets/Screenshot-2025-08-13-144255.png' | relative_url }}){: width="95%" }  
      * Paste the copied text **(both header and data)** into the text box in the GPS Upload  
      > Make sure the number of headers matches the number of data columns
      > Edit the Site ID  (ident) if needed

      **d)** Fixed Site GPS Upload  
      * Select the **GPS Type** , **Cruise Leg** , **Locatoion** , **Associated Site**, and **OCC Site**
      * Open the text file of the GPS waypoints copy the text file & paste into the loader  
      > Make sure to copy the **header <code>(ident,lat,long,time,ltime)</code>** and the data
      
        {: .note }
        Each OCC site should have its own GPS waypoint, but each waypoint can have multiple activities (CB activity, STR deployed, BMUs recovered, can all be at the same waypoint) **CTD/H2O activity needs its own waypoint**    
        
      * ![Screenshot of the REA GPS Entry Page]({{ '/assets/Screenshot-2025-08-13-145246.png' | relative_url }}){: width="95%" }  
      * To Submit Each Waypoint/Site Visit Separately:  
        * Copy and paste the GPS file header and data for a single waypoint
        > *E.g.* uploading waypoint 114 would look like pasting this:   
        **ident,lat,long,time,ltime**   
        **114,-14.257657,-169.435723,2023-08-08T22:09:43Z,2023-08-08 11:09:43**  
        * Select the GPS type, cruise, location (from dive nav sheet)
        * Select appropriate OCC_SITEID for the waypoint  
          * If unsure ask OCC team  
          * **If it’s a CTD/H2O activity you must leave OCC_SITEID blank and only select ASSOC_OCC_SITE (meaning CTD/H2O activity must be loaded separately)**

      * To Submit All Waypoints at Once: 
        * Open the text file of the GPS waypoints copy the text file & paste into the loader
        > Make sure to copy the **header <code>(ident,lat,long,time,ltime)</code>** and the data

          {: .note }
        You may want to consider uploading the waypoints separately since you **MUST** select an OCC site & the surveys  for each waypoint  
        If all waypoints are submitted at the same time under a single OCC site, you **MUST** update the site and survey information in the OCC Field Info Table after         

4. ## Updating the Site Visit Table  
  **a)** For StRS/Random Sites:
    * <u>Update Site Information:</u>
      * Navigate to the Site table in the mission application through: 
      > Data Services -> Data Entry -> Manual Site Entry **OR** Home Page > Site_Visit Entry

        {: .note }
      Make sure site data matches GPS download and what is on the data sheet
      * Enter “Reef Zone” and “Depth Bin” data for that site from the data sheet  
      * Save
    * <u>Update Field Activities:</u>
      * Enter all relevant metadata from the dive sheet, such as **Dive Number, Habitat Type, Visibility,** etc. 
      * Check the boxes for all activities that were conducted (*e.g.,* photoquads, SFM, etc) 
      
        {: .note }
      If SfM was conducted, checking the box and hitting ‘Save’ will create an SfM record, then metadata can be entered  
      *If accidentally created, this can be manually removed via Optical App*
      * Complete the QC step by checking the QC'd box and clicking Save. 

    **b)** For OCC Fixed Sites:
      * Navigate to the OCC field data in the mission application through: 
      > Data Services -> OCC Field Data Edit


      * Verify that the correct activities are checked and the proper OCC site is selected.
      * Update the GPS unit used during the survey.
      * Update the habitat type if it was provided on the dive sheet.
      * Save


## <center><span style="color: #264079;">Done!  <br> <span style="font-size: 150%;">☺︎  </span>  </span></center>


---

<center><a href="{{ '/docs/Data-Importing.html' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Back Data Entry
</a> <a href="{{ '/docs/Data-Manager.html' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Back to Data Manager Home
</a></center>

