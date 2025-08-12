---
layout: default
title: Document Your Data in InPort
parent: n
nav_order: 3
---
# How to Document Your Data in InPort

> This guide walks through each section required to properly document and update datasets in [InPort](https://www.fisheries.noaa.gov/inport/)
---


<style>
  .inport-tabs {
    display: flex;
    flex-wrap: wrap;
    border-bottom: 2px solid #ccc;
    margin-top: 2rem;
    font-family: sans-serif;
  }

  .inport-tab {
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

  .inport-tab.active {
    background-color: #ffffff;
    border-bottom: 2px solid white;
  }

  .tab-content {
    display: none;
    padding: 1rem;
    border: 1px solid #ccc;
    border-top: none;
    font-family: sans-serif;
  }

  .tab-content.active {
    display: block;
  }
</style>

<!-- Tab Headers -->
<div class="inport-tabs">
  <div class="inport-tab active" onclick="showTab('summary')">Summary</div>
  <div class="inport-tab" onclick="showTab('item-id')">Item Identification</div>
  <div class="inport-tab" onclick="showTab('keywords')">Keywords</div>
  <div class="inport-tab" onclick="showTab('location')">Physical Location</div>
  <div class="inport-tab" onclick="showTab('dataset-info')">Data Set Info</div>
  <div class="inport-tab" onclick="showTab('support-roles')">Support Roles</div>
  <div class="inport-tab" onclick="showTab('extents')">Extents</div>
  <div class="inport-tab" onclick="showTab('access-info')">Access Info</div>
  <div class="inport-tab" onclick="showTab('distribution-info')">Distribution Info</div>
  <div class="inport-tab" onclick="showTab('urls')">URLs</div>
  <div class="inport-tab" onclick="showTab('tech-env')">Tech Environment</div>
  <div class="inport-tab" onclick="showTab('data-quality')">Data Quality</div>
  <div class="inport-tab" onclick="showTab('data-management')">Data Management</div>
  <div class="inport-tab" onclick="showTab('lineage')">Lineage</div>
  <div class="inport-tab" onclick="showTab('acquisition')">Acquisition Info</div>
  <div class="inport-tab" onclick="showTab('child-items')">Child Items</div>
  <div class="inport-tab" onclick="showTab('related-items')">Related Items</div>
  <div class="inport-tab" onclick="showTab('catalog-details')">Catalog Details</div>
</div>

<!-- Tab Contents -->
<div id="summary" class="tab-content active"><p>Summary content here.</p></div>




<div id="item-id" class="tab-content"><p>
<strong>Item Identification</strong>
<ul>
  <li>
    <strong>Title:</strong> NCRMP: WHAT (metrics) + WHERE (region) + WHEN (from/to)
    <ul>
      <li><em>If Title includes “...since YEAR” change it to “...from YEAR to YEAR”</em></li>
      <img width="750" height=auto alt="Example:" src="{{ '/assets/screenshot-2025-08-01-120531.png' | relative_url }}" />

    </ul>
  </li>

  <li>
    <strong>Short Name:</strong> Add a short name if one isn’t already given 
    <ul>
      <li><em>If NCRMP, start with NCRMP: dataset</em></li>
      <img width="500" height=auto alt="Example:" src="{{ '/assets/screenshot-2025-08-01-122436.png' | relative_url }}" />

    </ul>
  </li>

  <li>
    <strong>Status:</strong> 
    <ul>
      <li>If NCRMP = ongoing</li>
      <li>If one-off project = completed</li>
    </ul>
  </li>

  <li>
    <strong>Creation Date:</strong> Month and year when the first dataset files included in the InPort record were submitted to NCEI
    <ul>
      <li><em>File date of data in <code>T:\DataManagement\NCEI Archive Packages\</code></em></li>
    </ul>
  </li>

  <li>
    <strong>Revision Date:</strong> Month and year you are revising the record with the new set of data
  </li>

  <li>
    <strong>Publication Date:</strong> Update YEAR to reflect when the dataset will be published or republished with new data
  </li>
    <div style="padding-left: 3em;">
        <em><img width="250" height=auto alt="Example:" src="{{ '/assets/Screenshot-2025-08-01-122859.png' | relative_url }}" /></em>
    </div>
    
  <li>
    <strong>Abstract:</strong> About the dataset — who, what, where, when, and a brief how
    <ul>
      <li>Who: PIFSC and ESD and CRCP (or NCRMP)</li>
      <li>Update to reflect latest mission/surveys</li>
      <li>Be sure to describe/emphasize the dataset to be archived (not the analysis, publication, or project).</li>
      <li>
        <em>Example:</em><br/>
        <blockquote>
        The data described here include <strong>XXXX</strong> data collected as part of NOAA's ongoing National Coral Reef Monitoring Program (NCRMP). These data were gathered around <strong>REGION AND/OR ISLAND(S)</strong> from <strong>DATE</strong> to <strong>DATE</strong> as a part of the NOAA Pacific Islands Fisheries Science Center (PIFSC), Ecosystem Sciences Division (formerly the Coral Reef Ecosystem Division) led NCRMP mission to <strong>REGION AND/OR ISLAND(S)</strong> in <strong>YYYY</strong>. The variables of <strong>XXXX</strong> were recorded by SCUBA divers during surveys at NCRMP climate stations. A select number of climate sites were chosen per island in hard-bottom habitat at 15-m depths in a stratified random fashion. To record <strong>XXXX</strong>, the divers... [brief overview of method]
        </blockquote>
      </li>
    </ul>
  </li>

  <li>
    <strong>Purpose:</strong> Why this dataset matters — what purpose does it serve?
    <ul>
      <li>
        <em>Example:</em><br/>
        <blockquote>
        Water temperature time series data aid in the monitoring of seawater temperature variability and are used to help scientists assess and understand how coral reefs monitored as part of the NOAA National Coral Reef Monitoring Program (NCRMP) are responding to thermal stress.
        </blockquote>
      </li>
    </ul>
  </li>

  <li>
    <strong>Notes:</strong>
    <ul>
      <li>Address any issues/questions/updates, then delete notes before submission</li>
      <li>You can also add a note for anything you’re not sure about, and we’ll figure out what to do with it.</li>  
      <li><strong>It should be deleted before the record is published and exported for NCEI </strong></li>
    </ul>
  </li>

  <li>
    <strong>Citation:</strong> Add any directly relevant publication citations (e.g., SOP, reports, summary briefs)
    <ul>
      <li>Drafts are okay — just indicate so</li>
    </ul>
  </li>

  <li>
    <strong>Supplemental Info:</strong> Big-picture context — if part of NCRMP, RAMP, or a one-off project, describe it here
    <ul>
      <li>
        <strong><u>Supplemental Info for Ecological Data:</u></strong><br/>
        <blockquote>
       <p>The NOAA National Coral Reef Monitoring Program (NCRMP) details a long term approach to provide an ecosystem perspective via monitoring climate, fish, benthic, and socioeconomic variables in a consistent and integrated manner. The NCRMP coordinates various NOAA Coral Reef Conservation Program (CRCP) biological, physical, and human dimensions activities into a cohesive NOAA-wide effort. Through the implementation of the NCRMP, NOAA is able to clearly and concisely communicate results of national-scale monitoring to national, state, and territorial policy makers, resource managers, and the public on a periodic basis.</p>

        <p> NCRMP is a framework for conducting sustained observations of biological, climate, and socioeconomic indicators at 10 priority coral reefs across the U.S. and its territories. This integrated approach consolidates monitoring of coral reefs under a uniform method in the Pacific, Atlantic, Caribbean, and the Gulf of Mexico for the first time. NCRMP is funded by the CRCP and supported by NOAA Fisheries, NOAA National Centers for Coastal Ocean Science (NCCOS), and many other partners. The PIFSC Ecosystem Sciences Division (ESD) at NOAA Fisheries is leading biological monitoring in the U.S. Pacific Islands Region. </p>

        <p> The biological component of NCRMP in the Pacific provides a triennial ecological characterization at a broad spatial scale of general reef condition for reef fishes, corals and benthic habitat (i.e., fish species composition/density/size, benthic cover, and coral density/size/condition). Innovative analysis techniques are then used to develop products that give fellow scientists, managers, decision makers and the public a better understanding of a region’s resources and how they are changing over time. </p> 

        </blockquote>
      </li>
      <li>
        <strong><u>Supplemental Info for Climate Data:</u></strong><br/>
        <blockquote>
        <p> The NOAA National Coral Reef Monitoring Program (NCRMP) details a long term approach to provide an ecosystem perspective via monitoring climate, fish, benthic, and socioeconomic variables in a consistent and integrated manner. The NCRMP coordinates various NOAA Coral Reef Conservation Program (CRCP) biological, physical, and human dimensions activities into a cohesive NOAA-wide effort. Through the implementation of the NCRMP, NOAA is able to clearly and concisely communicate results of national-scale monitoring to national, state, and territorial policy makers, resource managers, and the public on a periodic basis.</p>

        <p> NCRMP is a framework for conducting sustained observations of biological, climate, and socioeconomic indicators at 10 priority coral reefs across the U.S. and its territories. This integrated approach consolidates monitoring of coral reefs under a uniform method in the Pacific, Atlantic, Caribbean, and the Gulf of Mexico for the first time. NCRMP is funded by the Coral Reef Conservation Program (CRCP) and supported by NOAA Fisheries, NOAA National Centers for Coastal Ocean Science (NCCOS), NOAA’s Atlantic Oceanographic & Meteorological Laboratory (AOML), NOAA Coral Reef Watch, and many other partners. The Ecosystem Sciences Division (ESD) at NOAA Fisheries is leading in-situ climate monitoring in the U.S. Pacific Islands Region.</p>

        <p> The climate component of NCRMP in the Pacific provides a comprehensive view of climate change impacts on coral reef ecosystems and helps identify areas of resilience and vulnerability. The key indicators used to identify and monitor climate-driven trends include 1) thermal stress caused by changes in sea temperature, 2) ocean acidification resulting from changes in carbonate chemistry, and 3) ecological impacts by collecting data on coral growth rates, erosion, and community structure to understand the impacts of thermal stress and ocean acidification on the ecosystem. Each year, ESD scientists work closely with CRCP and partners during Reef Assessment and Monitoring Program (RAMP) missions to collect data using moored oceanographic and ecological instruments stationed at fixed sites in the Pacific Ocean, and water samples collected by divers. The in-situ data and satellite-based observations are also used in modeling efforts. Innovative analysis techniques are used to develop products that give fellow scientists, managers, decision makers and the public a better understanding of a region’s resources and how they are changing over time.</p>
        </blockquote>
      </li>
    </ul>
  </li>

  <li>
    <strong>DOI:</strong> Assigned only to NCRMP datasets (NCEI Collection) by CRCP
    <ul>
      <li>Usually applies only to NCRMP data</li>
      <li>
        To find the DOI:
        <ul>
          <li>Navigate to an existing dataset accession in the InPort record</li>
          <li>Go to Distribution Info → Accession URL → Documentation tab → NCEI Collection under Associated Resources</li>
          <li>Copy the Dataset Identifier (not the full link)</li>
          <li>
        Example: <code>10.7289/V59s6vcf5</code> (use the identifier only)
      </li>
        </ul>
      </li>
      
      <li>This is NOT the DOI for the related publication</li>
    </ul>
  </li>

  <li>
    <strong>DOI Registration Authority:</strong> NOAA
  </li>
</ul>

</p></div>





<div id="keywords" class="tab-content"><p>
  <strong>Keywords</strong>
 <ul>
    <li>InPort uses both <strong>CONTROLLED</strong> and <strong>UNCONTROLLED</strong> keywords.

      <ul>
        <li>Controlled keywords (GCMD thesauri) are required for CoRIS and help users find datasets on platforms like DATA.GOV and OneStop.</li>
        <li>Uncontrolled keywords (Theme) provide additional descriptive information.</li>
        <li>Keywords can be cloned from similar records to save time.</li>
      </ul>
    </li>

    <li><strong>Controlled Keywords:</strong>
      <ul>
        <li>Include:
          <ul>
            <li>Ecosystem Sciences Division as GCMD Data Center</li>
            <li>Coral Reef, Benthic, and other relevant GCMD Science Keywords</li>
            <li>Applicable GCMD Location, Instrument, and Platform Keywords</li>
          </ul>
        </li>
        <li>Add an ISO 19115 Topic Category (e.g., Biota, Oceans, Environment)</li>
       <div style="padding-left: 2em;">
             <em><img width="500" height=auto alt="Example:" src="{{ '/assets/Screenshot-2025-08-01-131806.png' | relative_url }}" /></em>
        </div>Screenshot-2025-08-01-131806
      </ul>
    </li>

    <li><strong>Uncontrolled Keywords (Theme):</strong>
      <ul>
        <li><a href="https://gcmd.earthdata.nasa.gov/KeywordViewer/scheme/all/ea7d9260-7e8f-4c53-89c4-f1b4bccc5a63">CoRIS Discovery Thesaurus</a> (required, only 1):
          <ul>
            <li>Numeric Data Sets > Benthic</li>
            <li>Numeric Data Sets > Biology</li>
            <li>Numeric Data Sets > Calcification Rate</li>
            <li>Numeric Data Sets > Chemistry</li>
            <li>Numeric Data Sets > Fish Census</li>
            <li>Numeric Data Sets > Oceanography</li>
            <li>Visual Images > Habitats</li>
          </ul>
        </li>
        <li><a href="https://data.nodc.noaa.gov/cgi-bin/iso?id=gov.noaa.nodc:ISO_19115_1">CoRIS Theme Thesaurus</a> (at least 1): match the ISO Topic Category.</li>
      </ul>
    </li>

    <li><strong>CRCP Project ID (if CRCP funded):</strong>
      <ul>
        <li><strong>NCRMP (2013+):</strong> 743 – National Coral Reef Monitoring Program</li>
        <li><strong>FY12:</strong> 587 – Pacific Reef Assessment and Monitoring Program</li>
        <li><strong>FY11 & earlier:</strong> 1221 – Pacific RAMP Biennial Monitoring</li>
      </ul>
    </li>

    <li><strong>NODC Thesauri:</strong>
      <ul>
        <li><strong>Observation Types:</strong> One observation type + one data type per metric.
          <ul>
            <li>e.g., survey, in situ, satellite data, visual assessment</li>
          </ul>
        </li>
        <li><strong>Data Types:</strong> e.g., percent cover, biomass, conductivity</li>
        <li>Use the NCRMP <a href="https://www.ncei.noaa.gov/data/oceans/ncei/ocads/metadata/NCRMP_NODC_Controlled_Vocabulary.xlsx">Controlled Vocabulary</a> as reference.</li>
      </ul>
    </li>

    <li><strong>Project, Institution, and Exclusion Keywords:</strong>
      <ul>
        <li><strong>NODC Project Thesaurus:</strong>
          <ul>
            <li>Coral Reef Conservation Program</li>
            <li>National Coral Reef Monitoring Program</li>
            <li>Pacific RAMP</li>
          </ul>
        </li>
        <li><strong>NODC Submitting Institution:</strong> e.g., US DOC, NOAA, NMFS, PIFSC, CRED</li>
        <li><strong>PARR Exclusion (optional):</strong> e.g., Non-Federal Funding, Legacy Data Set</li>
      </ul>
    </li>

    <li><strong>Instrument:</strong>
      <ul>
        <li>TYPE = INSTRUMENT</li>
        <li>Use NODC INSTRUMENT TYPES THESAURUS if possible</li>
        <li>Examples: ADCP, CTD, fluorometer, GPS, STR, CTD etc.</li>
      </ul>
    </li>

    <li><strong>Platform:</strong>
      <ul>
        <li>Use <a href="https://www.ncei.noaa.gov/access/inport/item/1251659">NODC PLATFORM NAMES THESAURUS</a></li>
        <li>Examples: Hi‘ialakai, Oscar Elton Sette, Small Vessels</li>
        <li>TYPE = PLATFORM</li>
      </ul>
    </li>

    <li><strong>Spatial/Place:</strong>
      <ul>
        <li><a href="https://www.coris.noaa.gov/data/supportrngdocs.html#keywords">CoRIS Place Thesaurus</a>: 1+ pair per region</li>
        <li>One for COUNTRY/TERRITORY and one for OCEAN BASIN</li>
        <li>Examples:
          <ul>
            <li>COUNTRY/TERRITORY = Northern Mariana Islands</li>
            <li>OCEAN BASIN = Western Pacific Ocean</li>
          </ul>
        </li>
        <li>Also add keywords from:
          <ul>
            <li><a href="https://gcmd.earthdata.nasa.gov/KeywordViewer/scheme/all/a4523ae1-d49a-45cf-98e0-eed261e0ac8b">Pacific Country Thesaurus</a></li>
            <li><a href="https://gcmd.earthdata.nasa.gov/KeywordViewer/scheme/all/fb050d4f-ec8e-43ed-89f0-393f209c53c3">Pacific Ocean Thesaurus</a></li>
            <li>NODC SEA AREA NAMES THESAURUS</li>
          </ul>
        </li>
      </ul>
    </li>
  </ul></p></div>





<div id="location" class="tab-content"><p>Physical Location content here.</p></div>
<div id="dataset-info" class="tab-content"><p>Data Set Info content here.</p></div>
<div id="support-roles" class="tab-content"><p>Support Roles content here.</p></div>
<div id="extents" class="tab-content"><p>Extents content here.</p></div>
<div id="access-info" class="tab-content"><p>Access Info content here.</p></div>
<div id="distribution-info" class="tab-content"><p>Distribution Info content here.</p></div>
<div id="urls" class="tab-content"><p>URLs content here.</p></div>
<div id="tech-env" class="tab-content"><p>Tech Environment content here.</p></div>
<div id="data-quality" class="tab-content"><p>Data Quality content here.</p></div>
<div id="data-management" class="tab-content"><p>Data Management content here.</p></div>
<div id="lineage" class="tab-content"><p>Lineage content here.</p></div>
<div id="acquisition" class="tab-content"><p>Acquisition Info content here.</p></div>
<div id="child-items" class="tab-content"><p>Child Items content here.</p></div>
<div id="related-items" class="tab-content"><p>Related Items content here.</p></div>
<div id="catalog-details" class="tab-content"><p>Catalog Details content here.</p></div>

<script>
  function showTab(tabId) {
    document.querySelectorAll('.tab-content').forEach(tab => {
      tab.classList.remove('active');
    });
    document.querySelectorAll('.inport-tab').forEach(tab => {
      tab.classList.remove('active');
    });
    document.getElementById(tabId).classList.add('active');
    event.target.classList.add('active');
  }
</script>









