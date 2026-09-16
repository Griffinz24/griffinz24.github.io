---
layout: page
title: Lake Mattamuskeet
description: Sensor Data Management
img: assets/img/LMfoggy.jpg
importance: 1
category: Data
related_publications: false
---

lake Mattamuskeet is the largest natural lake in North Carolina.
The lake, which is located in Hyde County, has a surface area of over 40,000 acres, and has an average depth of only ~1 foot.
Lake Mattamuskeet is 

Due to extensive hydrologic modification of the region and the significant agricultural land use in the region, the lake faces major challenges with eutrophication.
Eutrophication is the presence of excess nutrients within a body of water which causes major, compounding problems for the water body.

This diagram, by Britannica (https://www.britannica.com/science/eutrophication), easily demonstrates this process.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/EutrophicationProcess.png" title="Eutrophication process" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is a figure of a common eutrophication process. Britannica, (https://www.britannica.com/science/eutrophication).
</div>

Because of these conditions, monitoring water quality and similar water parameters becomes incredibly valuable.
Dr. Randall Etheridge, A researcher and professor in East Carolina University's Center for Sustainable Energy and Environmental Engineering, has installed multiple sensors around the area.
These sensors, which include tilt meters, low-cost, real-time LoRaWAN water level sensors, and traditional HOBO water level loggers.

Over the 16+ monitoring locations, each location has a tilt meter sensor (collecting flow and heading) and a low-cost water level sensor.
Each sensor measures a reading every 15 minutes.
Because of the amount of data per location, data becomes messy, very quickly.
By utilizing the programming tool, R, I have been able to effectively "solve" this issue.

This process can easily be broken down into the three key steps of the process.
First, gathering data from tilt meters, which creates the location ID's for the sites.
Next, gathering data from the associated location tilt meters.
Finally, all the data is compiled into an Excel file for each location.
 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/TiltMeterPNG.png" title="Tilt meter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This steps gathers data from the tilt meter and assigns the location.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/WaterLevelPNG.png" title="Water level" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This step gathers data from the water level sensors.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FinishedComboPNG.png" title="Finished combo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This step is where all collected data is "mashed" together by location.
</div>


While this is an simple breakdown, the refinement of data sources and output was a substantial challenge in a successful script.
This project was my first jumping off point for working in R and has greatly improved my ability to handle complicated data management.
