---
layout: page
title: Builing a database backend for a WebGIS
description: Creating a spatial database for an example festival
img: assets/img/oktoberfest.png
importance: 5
category: work
related_publications: false
---

### Summary

This project involved designing and building the spatial database backend for a proposed mobile WebGIS application for the Munich Oktoberfest. The goal was to create a robust database that could store and manage various types of spatial and temporal data relevant to the festival, such as the locations of tents, rides, and amenities, as well as event schedules. The final database is capable of answering complex, real-time user queries to enhance the visitor experience, for example, by finding nearby events or amenities based on a user's current location and time.

---

### Key Points

**Data Preparation and Digitization:** Since no official spatial data was available, the initial phase involved data creation. Base data for the Theresienwiese area was downloaded from OpenStreetMap (OSM) and then cleaned. Additional features were manually digitized in QGIS using an official Oktoberfest map as a reference, resulting in a complete and accurate set of spatial layers for all festival entities.

<div class="row">
<div class="col-sm mt-3 mt-md-0">
{% include figure.liquid loading="eager" path="assets/img/oktoberfest_map_comparison.png" title="Comparison of the official map and the manually digitized data" class="img-fluid rounded z-depth-1" %}
</div>
</div>
<div class="caption">
On the left is the official Oktoberfest map used for reference; on the right is the final, manually mapped data in QGIS.

</div>

<br>

**Database Design and Structure:** A physical data model was designed to organize the various festival entities, including tents, rides, events, toilets, ATMs, and visitors. A central locations table was created to manage all physical entities, simplifying relationships and queries. The database schema was implemented in PostgreSQL with PostGIS, using pgAdmin's ERD tool to visualize the final structure.

<div class="row">
<div class="col-sm mt-3 mt-md-0">
{% include figure.liquid loading="eager" path="assets/img/oktoberfest_db_model.png" title="Physical data model of the Oktoberfest database" class="img-fluid rounded z-depth-1" %}
</div>
</div>
<div class="caption">
A graphical overview of the database schema, showing the tables and their relationships.

</div>

<br>

**Spatio-Temporal Queries:** The database was specifically designed to handle spatio-temporal queries from a visitor's perspective. Tables for visitors, events, and locations include timestamp and geometry columns, enabling dynamic queries that consider both the user's location and the current time.

<div class="row">
<div class="col-sm mt-3 mt-md-0">
{% include figure.liquid loading="eager" path="assets/img/oktoberfest_query1.png" title="Query to find nearby events that have not ended yet" class="img-fluid rounded z-depth-1" %}
</div>
</div>
<div class="caption">
An example query that finds all events within 500m of a visitor ("Anna") that are happening on the same day and have not yet finished.

</div>

<br>

**Practical Application Scenarios:** Several example queries were developed to demonstrate the database's functionality. These scenarios showcase how the app could help a visitor find a tent with a specific capacity level, locate family-friendly rides within a certain area ("Oide Wiesn"), or discover all points of interest within a short walking distance.

<div class="row">
<div class="col-sm mt-3 mt-md-0">
{% include figure.liquid loading="eager" path="assets/img/oktoberfest_query2.png" title="Query to find tents based on capacity and distance" class="img-fluid rounded z-depth-1" %}
</div>
</div>
<div class="caption">
A query for a visitor ("Maria") looking for tents with a capacity utilization between 65% and 91%, ordered by distance.

</div>

<div class="row">
<div class="col-sm mt-3 mt-md-0">
{% include figure.liquid loading="eager" path="assets/img/oktoberfest_qgis_output.png" title="Visualizing a query result in QGIS" class="img-fluid rounded z-depth-1" %}
</div>
</div>
<div class="caption">
A map-based visualization of the query result, showing Maria's position and the suitable tents colored by distance.

</div>

<br>

Full documentation:

<iframe src="/assets/pdf/exercise13_stobbelaar.pdf" width="100%" height="600px" style="border: none;">
<a href="/assets/pdf/exercise13_stobbelaar.pdf">Download PDF</a>.
</iframe>
