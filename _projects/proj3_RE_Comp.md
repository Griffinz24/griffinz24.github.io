---
layout: page
title: Real Estate Comps Dashboard
description: Automated Commercial Real Estate Visualization
img: assets/img/RE_Dashboard.jpg
importance: 2
category: Data
related_publications: false
---

Commercial real estate evaluation relies heavily on accurate comparable sales and lease data ("comps"). However, tracking transaction history across multiple asset classes (Office, Industrial, Retail, Land, Hotel) over several years often leaves data fragmented across dozens of separate spreadsheets and standard files.

To solve this issue and streamline property valuation workflows, I developed an interactive **R Shiny** web application that standardizes multi-year Excel spreadsheets, performs address validation, geocodes real property data, and present key metrics via a dynamic dashboard.

---

### Key Technical Pipeline

The workflow can be broken down into three main operational phases:

1. **Multi-Year Excel Ingestion & Harmonization**
2. **Regex Address Validation & Automated Geocoding**
3. **Interactive Exploration & Visualization (Shiny, Leaflet, DT)**

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/RE_Addresses.jpg" title="Data Import from messy Excel file" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Automated cross-year validation and dynamic schema alignment across 8 distinct real estate asset types (2022–2026).
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/RE_SaleGraph.jpg" title="Interactive Sales Graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Easy comparison and evaulation of metrics related to real estate purchases.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/RE_Dashboard.jpg" title="Interactive Map" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Interactive Leaflet (openstreetmap) geospatial mapping, transaction trend analytics via `ggplot2`, and search-indexed data tables using `DT`.
</div>

---

### Features & Implementation Highlights

* **Automated Import & Column Normalization:** The script scans multi-sheet workbooks across 5 years of data (2022–2026). It automatically harmonizes variable data types (e.g., character forcing on mixed format dates, escalations, and rates) and binds them into a consolidated master dataset.
* **Robust Address Filtering:** Built-in regular expressions screen street suffixes (`Ave`, `Rd`, `Dr`, `Blvd`, etc.) and filter out incomplete entries or placeholder street numbers (`000`, `9999`) prior to map rendering.
* **API Geocoding with Disk Caching:** Utilizes `tidygeocoder` targeting the U.S. Census API. Geocoded coordinates are cached locally into a `.rds` file to prevent redundant external API calls across application restarts.
* **Interactive Shiny UI:** 
  * **Data Explorer:** Offers real-time property type and year filtering with column-level search powered by `DT`.
  * **Time Series Analysis:** Dynamically tracks transaction volume trends over time across asset categories using `ggplot2`.
  * **Interactive Geospatial Mapping:** Displays color-coded property markers via `leaflet` with custom popup overlays showing price points and lease characteristics. Included error logging allows users to view excluded or failed address records.

This project expanded my capabilities in building production-ready R Shiny dashboards, managing external API queries, and handling unstructured spatial data.