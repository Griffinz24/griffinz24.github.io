---
layout: page
title: Lake Mattamuskeet Data Management
description: with background image
img: assets/img/LMfoggy.jpg
importance: 1
category: work
related_publications: false
---

Lake Mattamuskeet is a unique, understudied natural lake in Eastern North Carolina. ADD MORE ABOUT LM HERE.



To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/TiltMeterPNG.png" title="Tilt meter" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is tilt meter.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/WaterLevelPNG.png" title="Water level" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is water level.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/FinishedComboPNG.png" title="Finished combo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This is combo.
</div>


Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

