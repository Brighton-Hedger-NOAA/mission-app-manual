---
layout: default
title: 'Goal 4: InPort Metadata Record Review'
parent: Archive Refresher & Workshop
nav_order: 5
---

# Update InPort Metadata Record
### This is for updating existing InPort metadata records with your additional data. The tabs in  <span style="color: #003366; font-weight: bold; background-color: #e6f2ff; border: 1px solid #b3d7ff; padding: 2px 6px; border-radius: 4px;">blue</span> indicate sections that typically require updates for this workflow. Click each tab to see the required actions.

If starting from scratch or need some extra guidance, click <a href="https://docs.google.com/document/d/1kijqSQbISTcOO9JQ_5_AtAZuVvLc-y0y0v-KlKeO1sY/edit?usp=sharing" target="_blank" rel="noopener noreferrer"> <strong>here</strong> </a> for an in depth InPort guide!

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
    font-weight: normal; /* Default font weight */
    font-size: 0.9rem;
    color: #333; /* Default color for non-required tabs */
    cursor: pointer;
  }
  
  /* Style for required tabs */
  .inport-tab.required {
    font-weight: bold;
    color: #003366; /* Dark blue for emphasis */
    background-color: #e6f2ff; /* Light blue background */
  }

  .inport-tab.active {
    background-color: #ffffff;
    border-bottom: 2px solid white;
    position: relative;
    top: 1px;
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

<div class="inport-tabs">
  <div class="inport-tab" onclick="showTab('summary')">Summary</div>
  <div class="inport-tab required active" onclick="showTab('item-id')">Item Identification</div>
  <div class="inport-tab required" onclick="showTab('keywords')">Keywords</div>
  <div class="inport-tab" onclick="showTab('location')">Physical Location</div>
  <div class="inport-tab required" onclick="showTab('dataset-info')">Data Set Info</div>
  <div class="inport-tab required" onclick="showTab('support-roles')">Support Roles</div>
  <div class="inport-tab required" onclick="showTab('extents')">Extents</div>
  <div class="inport-tab required" onclick="showTab('access-info')">Access Info</div>
  <div class="inport-tab required" onclick="showTab('distribution-info')">Distribution Info</div>
  <div class="inport-tab required" onclick="showTab('urls')">URLs</div>
  <div class="inport-tab" onclick="showTab('tech-env')">Tech Environment</div>
  <div class="inport-tab required" onclick="showTab('data-quality')">Data Quality</div>
  <div class="inport-tab" onclick="showTab('data-management')">Data Management</div>
  <div class="inport-tab required" onclick="showTab('lineage')">Lineage</div>
  <div class="inport-tab" onclick="showTab('acquisition')">Acquisition Info</div>
  <div class="inport-tab required" onclick="showTab('child-items')">Child Items</div>
  <div class="inport-tab required" onclick="showTab('related-items')">Related Items</div>
  <div class="inport-tab" onclick="showTab('catalog-details')">Catalog Details</div>
</div>

<div id="summary" class="tab-content"><p>Summary will populate from other tabs. No information is needed.</p></div>

<div id="item-id" class="tab-content active">
  <p>After updates to your data and data dictionary are complete, review the following content in this section.</p>
  <ul>
    <li><strong>Update Publication Date:</strong> Update to the year you are currently updating the record.</li>
   <li>
  <strong>Update Abstract:</strong> Update the abstract if needed.
  <p style="margin-left: 20px; font-style: italic;">
    For example: 'in 2024 we started collecting x data, captured by column x_col'
  </p>
</li>
    <li><strong>Add Citations:</strong> Add any new relevant citations, reports, or publications.</li>
  </ul>
</div>

<div id="keywords" class="tab-content">
  <p>Review the keywords associated with this record.</p>
  <ul>
    <li>Check if any new keywords need to be added to better describe the dataset.</li>
  </ul>
</div>

<div id="location" class="tab-content"><p>No information typically needs to be entered or changed in this section for this workflow.</p></div>

<div id="dataset-info" class="tab-content">
  <p>Review the Maintenance and Update Frequency.</p>
  <ul>
    <li>You can update the <strong>Maintenance Note</strong> to things like 'Updated as new data is added'.</li>
  </ul>
</div>

<div id="support-roles" class="tab-content">
  <p>Update the points of contact and roles for this dataset.</p>
  <ul>
    <li>Are you a new archivist for this dataset? Add yourself.</li>
    <li>Has anyone associated with this record left the organization? Update if needed.</li>
  </ul>
</div>

<div id="extents" class="tab-content">
  <p>Define the geographic and temporal boundaries of the dataset.</p>
  <ul>
    <li><strong>Add Timeframe:</strong> Use the minimum and maximum dates directly from the dataset file to define the time range for the region.</li>
    <li><strong>Bonus Check:</strong> Verify that the maximum latitude and longitude from your dataset fall within the current bounding box defined in the InPort record.</li>
  </ul>
</div>

<div id="access-info" class="tab-content">
  <p>Review the data access and use constraints.</p>
  <ul>
    <li>Update the example citation located in the <strong>Data Use Constraints</strong> field.</li>
  </ul>
</div>

<div id="distribution-info" class="tab-content">
  <p>Update information on how the data is distributed.</p>
  <ul>
    <li>Add a placeholder for the new NCEI accession that will be associated with this new dataset.</li>
    <li>Use the dataset's filename for the placeholder name.</li>
    <li>Use the URL <a href="https://accession.nodc.noaa.gov/#" target="_blank" rel="noopener noreferrer">https://accession.nodc.noaa.gov/#</a> and add a brief description.</li>
  </ul>
</div>

<div id="urls" class="tab-content">
  <p>Check all supplemental URLs for accuracy.</p>
  <ul>
    <li>Is there anything that should be included here that isn't already?</li>
    <li>Are there any dead links that need to be removed or updated?</li>
    <li>Examples include links to GitHub repositories, technical memoranda, SOPs, etc.</li>
  </ul>
</div>

<div id="tech-env" class="tab-content"><p>No information typically needs to be entered or changed in this section for this workflow.</p></div>

<div id="data-quality" class="tab-content">
  <p>Provide information on the quality and accuracy of the data. Update this section if needed based on the new data being added.</p>
</div>

<div id="data-management" class="tab-content"><p>No information typically needs to be entered or changed in this section for this workflow.</p></div>

<div id="lineage" class="tab-content">
  <p>Describe the process steps and data sources used to create the dataset. This is similar to a Standard Operating Procedure (SOP).</p>
  <ul>
    <li>If there is a publicly available SOP for this process, you can summarize it in a sentence or two and provide a direct link instead of writing everything out.</li>
    <li>Add any new SOPs if they are relevant to the new data.</li>
  </ul>
</div>

<div id="acquisition" class="tab-content"><p>No information typically needs to be entered or changed in this section for this workflow.</p></div>

<div id="child-items" class="tab-content">
  <p>This section is the <strong>Data Dictionary</strong>, also referred to as the "InPort record entity." You reviewed and updated this in the previous step, so this section should be accurate.</p>
</div>

<div id="related-items" class="tab-content">
  <p>Link to other relevant records within InPort.</p>
  <ul>
    <li>Are there any related InPort records that are not yet listed?</li>
    <li>If so, add them as a <strong>Cross-Reference</strong>.</li>
  </ul>
</div>

<div id="catalog-details" class="tab-content"><p>No information typically needs to be entered or changed in this section for this workflow.</p></div>


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

---

## <center>After reviewing all metadata sections, you are ready for the next phase.</center>

---

<center>
<a href="{{ '/docs/Data-Review.html' | relative_url }}" class="btn btn-secondary fs-6 mb-4 mb-md-0">
  ← Previous: Data Review
</a>
<a href="{{ '/docs/S2N-Prep.html' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Next: S2N Prep →
</a></center>