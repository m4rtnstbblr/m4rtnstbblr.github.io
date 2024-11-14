---
layout: page
title: Building a spatial database infrastructure
description: MIGE - MIgrations GErmany a interactive dashboard
img: assets/img/MIGE.jpg
importance: 1
category: work
related_publications: false
---

### Summary

The **MIGE (MIgrations GErmany) project** aims to create a spatial data infrastructure (SDI) to visualize migration data in Germany, leveraging an open GIS architecture. The project involved multiple phases, including data acquisition from reliable sources like Eurostat and Destatis, data preprocessing and integration, and implementation into a PostGIS database. The SDI system allows the data to be accessed as web services, enabling interactive and user-friendly presentations.

#### Key Points
- **Data Sources & Processing**: Population migration data was cleaned and spatially linked using NUTS codes, which were essential for dashboard visualizations.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sdi_prep.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Generalized overview of data preparation
</div>

<br>

- **SDI Architecture**: A GIS-based infrastructure (ESRI) was established to facilitate the sharing and visualization of migration data.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sdi_architecture_simple.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    General architecture overview
    </div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sdi_architecture.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    SDI architecture overview
    </div>
<br>


- **Dashboards**: Three dashboards illustrate intercountry migration, intracountry movements, and population changes across Germany, offering agencies intuitive, real-time insights into migration trends. Down below you can try the intercountry dashboard out. 


<iframe src="https://zgis.maps.arcgis.com/apps/dashboards/8531c6072efd44d693cb6adf94d22a0f" width="100%" height="600px" style="border: none;">



<br>

**Full documentation:**
<iframe src="/assets/pdf/SahinovicStobbelaar_MIGE_FinalDocumentation.pdf" width="100%" height="600px" style="border: none;">
    <a href="/assets/pdf/SahinovicStobbelaar_MIGE_FinalDocumentation.pdf">Download PDF</a>.
</iframe>




