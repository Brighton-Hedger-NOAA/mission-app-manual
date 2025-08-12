---
layout: default
title: 'Goal 3: Dataset/Data Dictionary Review'
parent: Archive Refresher & Workshop
nav_order: 4
---

# Dataset/Data Dictionary Review
### In this step, you will QC your dataset and data dictionary. This ensures the data is accurate, well-described, and ready for the metadata update process.

---

## Data Review Checklist

- [ ] **Are the filenames named appropriately?**
> Follow the standard naming convention: <strong>ESD_NCRMP_datastream_year_region</strong> (or compare to past archive packages).

- [ ] **Are there null values that aren't accounted for in the data dictionary?**
> If null values are present and are not an error, make sure to explain them in the InPort child item (the data dictionary section).

- [ ] **Are there new columns compared to last year, new data captured, or old data not captured?**
> - If needed, update the InPort child item.
> - For big changes, you may need to reupload the dataset or copy the most recent InPort record. (Ask Lori for help).

- [ ] **Do the columns match the current data dictionary?**
> If not, determine why columns might be missing or why they need to be updated in the InPort child item.

- [ ] **After reviewing, confirm the data dictionary is updated and captures all columns in the new dataset, then export it to a CSV file.**

---

## <center>Once your data and dictionary are reviewed, you can proceed.</center>

---

<center>
<a href="{{ '/docs/InPort-Set-Up.html' | relative_url }}" class="btn btn-secondary fs-6 mb-4 mb-md-0">
  ← Previous: Set Up InPort
</a>
<a href="{{ '/docs/InPort-Metadata-Review.html' | relative_url }}" class="btn btn-custom fs-6 mb-4 mb-md-0">
  Next: InPort Metadata Review →
</a></center>