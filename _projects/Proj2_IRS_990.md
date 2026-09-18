---
layout: page
title: Nonprofit Performance Analysis
description: Utilizing IRS Data for Insights
img: assets/img/IRS_Logo.png
importance: 2
category: Data
related_publications: false
---

501(c)3 nonprofits serve an incredibly valuable purpose accross a wide range of fields.
Despite this, ensuring that a nonprofit is truly a "non profit" is valuable for donors and volunteers.
Additionally, analyzing nonprofit performance can be incredibly vital for nonprofit employees and managers.

While gathering this data can be done internally, it is also shared publically through IRS form 990, Return of Organization Exempt from Income Tax.
This required document shares many relevant features about tax-exempt organizations, like nonprofits.
Of all the fields, some of the most valuable include:

    Total Employees
    Total Volunteers
    Total Revenue
    Total expenses
    and more!

While this data can be incredibly helpful, sorting through the pdf form can be time consuming and inefficient. 
Because the each year's submittal is more than 45 pages, time commitment adds up quickly.
This is where implementing code can be **huge**.
For example, here is a sample of a page 1 of a 2024 completed IRS 990 from the nonprofit, Sound Rivers.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/Sound_Rivers_990.png" title="Sound Rivers 990" class="img-fluid rounded z-depth-1 w-50" %}
    </div>
</div>
<div class="caption">
    This is an example of the first page of a 2024 form 990 from Sound Rivers.
</div>

While it may _sound_ easy to just extract the text from a pdf, in reality it is specific and complicated.
To accomplish this task, you must use "scraping".
Scraping is the act of extract text (or other information) from a given source.
The script I wrote utilized multiple key "scraping" packages in R.
These packages include:

    
    pdftools
    tesseract
    openxlsx
    stringr
    dplyr
    htmlwidgets
    

These open source tools, along with trial and error, were able to help me create this tool!
Because running the script allows for quick analysis of decades of information, you can quickly pinpoint trends.
To analyze these trends I utilized Plotly to create a dynamic, interactive plot.


<iframe 
    src="{{ '/assets/html/SoundRiversMoney.html'}}" 
    frameborder="0" 
    scrolling="no" 
    style="width: 100%; height: 500px; border: none;">
</iframe>
<div class="caption">
    This plot shows a sample plot from scraping multiple years of 990s. This graph shows total revenue, total expenses, and net.
</div>


Taking a quick glance at this plot can show how quickly an individual can gather important information relevant to business success.
Alternately, you can use this insight to look at how a nonprofit has grown over time or expanded its reach/contributions!


<iframe 
    src="{{ '/assets/html/SoundRiversPeople.html'}}" 
    frameborder="0" 
    scrolling="no" 
    style="width: 100%; height: 500px; border: none;">
</iframe>

<div class="caption">
    This plot shows a sample plot from scraping multiple years of 990s. This graph shows total volunteers (right y axis) and total contributions from membership dues (left y axis).
</div>

Utilizing public records is an excellent data source, no matter what sector you are in.
Because you can derive so much data from public sources, you can identify the aspects that will be most impactful for *you*.

