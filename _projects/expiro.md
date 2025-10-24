---
layout: page
title: ExPiRo -- An External Pipe Crawling Robot
description: 
img: assets/img/expiro_2.jpg
importance: 1
category: work
related_publications: true
---


<style>
.equal-height-img {
  height: 220px;               /* uniform visual height */
  width: 100%;
  object-fit: contain;         /* keep full image visible, no cropping */
  background-color: #fafafa;   /* light neutral background for padding */
  border-radius: 8px;          /* consistent rounded corners */
  box-shadow: 0 2px 6px rgba(0,0,0,0.1); /* soft shadow */
  padding: 4px;                /* optional small inner padding */
}
</style>

<h2>Introduction</h2>

In modern society, pipeline systems play a crucial role in conveying gas, water, sewage. Pipelines are used for long-distance transportation of a liquid or gas. The use of pipelines are useful for transporting water for drinking or irrigation over long distances when it needs to move over hills, or where canals or channels are poor choices due to considerations of evaporation, pollution, or environmental impact.

Pipeline robots are at interest of local and international researchers for a long time as it serves the purpose of autonomous monitoring of pipelines internally and externally, in some cases operating as a substitute for human workers in pipeline maintenance related tasks. External pipeline robots are commonly used for pipe networks laid above the ground level and sometimes with a waterproof setup can also be used to monitor underwater pipeline networks as well.

<h2>Robot Design</h2>

ExPiRo utilizes wheeled locomotion for traveling on the curved surfaces of pipelines. It has a passive clutching mechanism based on a four-bar linkage that can adapt to the diameter of the pipe during locomotion. The wheels which will be addressed as rollers are designed to obtain the maximum grip between the robot and the pipe surfaces. The robot has a total of 8 driven rollers to provide propulsion. The robot structure has been optimized to reduce weight while maintaining required structural integrity.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/expiro_1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/expiro_2.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Control System</h2>

Reaching a certain goal position on a pipeline system is a crucial capability for an external pipe crawling robot. Therefore, a PID controller which controls the position of the robot was designed. An ADAMS-MATLAB co-simulation was conducted to tune the gains of the controller. The tuned system demonstrated a significant ability for accurate goal reaching.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/expiro_3.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/expiro_4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>
