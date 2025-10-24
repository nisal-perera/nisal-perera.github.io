---
layout: page
title: ProteanBot -- A Novel Mobile Platform for Healthcare Sector
description: 
img: assets/img/proteanbot_real.jpg
importance: 1
category: work
related_publications: true
---

<h2>Context</h2>
In Sri Lankan healthcare sector, the patient facilitation process is done by medical staff. Therefore, the unavailability of dedicated staff members for patient facilitation through delivering medication, medical samples and even documents has forced the nursing staff or any other personnel with different expertise to carry out such tasks. This has caused problems in human resource allocation at the ‘National Institute for Nephrology Dialysis and Transplantation, Sri Lanka’ due to the limited staff members. The issues concerning transportation of dialysis solutions within the hospital were identified during a discussion with officials at the institute.

In catering the same problem, the international healthcare sectors have moved on to the usage of robotics. Hence several mobile platforms have been developed commercially. However, these mobile robots might not be compatible within the local healthcare sector due to reasons such as unevenness of floors, unscheduled tasks, dimensional differences/non-uniform spacing within wards etc.

With these issues, the adoption of readily available products has been difficult. Furthermore, the cost of a customized product can be high. Due to these reasons there is a lack of high end robots within the local healthcare sector. The mobile platform was developed in this project will consist of a mechanical system and algorithms that can cater the needs of Sri Lankan healthcare sector. 

<h2>Introduction</h2>

Maneuverability, controllability and stability are fundamental characteristics of a wheeled mobile robot. The robots footprint is a key factor that determines the stability. Furthermore, it can often dictate the robots navigation abilities as well. Therefore, a wheeled mobile robot having the ability to vary its footprint can have flexible stability and the ability to navigate through space restricted areas. The currently available commercial mobile robots do not have the ability to vary footprint/size. In general a hospital environment is usually crowded and space restricted. The variable footprint capability is especially useful in such scenarios, where robot is navigating through a crowded environments with a payload. his project was focused on designing and developing a footprint varying mobile robot with sufficient maneuverability and payload carrying capacity.

<h3><u>Aim</u></h3>
Enhancing the patient facilitation of Sri Lankan hospitals, by introducing an autonomous transportation system for indoor logistic tasks.

<h3><u>Objectives</u></h3>
-To study on existing mobile platforms to identify suitable wheel configurations to carry the required payload and improve the maneuverability.
-To design and develop the mechanical system of the mobile platform with variable footprint feature.
-To develop a controller using suitable control algorithms to achieve autonomy.
-To validate and test.

<h2>ProteanBot Design</h2>

A novel transformable chassis with variable footprint capability and an actuation mechanism was designed. A key feature of ProteanBot is that the chassis transformation can be done using a single actuator. The proposed design can have footprint reductions up to 51% ideally.  The mobile platform also consists of a compatible suspension system to reduce ground induced vibrations. The fabricated prototype demonstrated footprint reductions up to 40%.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proteanbot_cad.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/proteanbot_real.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>



<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
