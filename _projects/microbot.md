---
layout: page
title:  Microrobotic Systems and Magnetic Microactuators
description: 
img: assets/img/publication_preview/swim_microbot.gif
importance: 3
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

.featured-video {
  max-width: 900px;
  margin: 2rem auto;
}

.featured-video figure {
  aspect-ratio: 16 / 9;
  margin: 0;
}

.featured-video iframe {
  width: 100%;
  height: 100%;
  border-radius: 8px;
}
</style>

<div class="related-publication-citations" style="display: none;">
  {% cite app122211542 %}
  {% cite 9525635 %}
  {% cite kankanige2022 %}
</div>

<h2>Introduction</h2>

At the intersection of microfabrication, soft materials, and magnetics, my research focused on developing magnetic microactuators and microscale robotic systems for next-generation biomedical and lab-on-a-chip (LOC) applications. These miniature devices leverage soft magnetic materials and flexible polymer structures to achieve controlled motion and force output under low magnetic fields, enabling untethered actuation and manipulation at the microscale.
Our work emphasized scalable actuator design, where modular magnetic structures and compliant beams are optimized for compactness, range of motion, and force efficiency. By integrating these actuators into microswimmers and micro-manipulation platforms, I explored new frontiers in controlled locomotion and object handling in viscous or non-Newtonian fluid environments.

<h2>Methodology</h2>

The proposed magnetic microactuator was designed to achieve compactness, high force output, and controllable motion under low magnetic field strengths. The actuator consists of three soft magnetic Ni-Fe (4750) blocks interconnected by two semi-circular Polydimethylsiloxane (PDMS) beams. A parametric design approach was employed to determine optimal dimensions for the magnetic blocks and compliant beams, balancing mechanical flexibility and magnetic flux density. The structural design was modeled using finite element analysis (FEA) to evaluate stress distribution, displacement response, and magnetic field interactions. A coupled magnetic–mechanical simulation framework was developed to study actuator deformation under varying magnetic field strengths. The simulation incorporated the nonlinear magnetic properties of Ni-Fe 4750 and the hyperelastic characteristics of PDMS. The actuator was exposed to uniform magnetic fields in the range of 80–160 kA/m, and the resulting displacements and forces were computed. The model outputs were analyzed to identify linearity in actuation characteristics and to predict the maximum displacement (111.6 µm) and force output (404.3 nN) under no-load conditions.

To evaluate its functional potential, the actuator was integrated with a microswimmer platform featuring an artificial appendage performing rowing motion. The actuator’s angular displacement and stroke angle were analyzed to assess its suitability for untethered locomotion in viscous media. The fluid–structure interaction (FSI) simulations were performed to model the interaction between the flexible appendage and a non-Newtonian fluid, providing quantitative insight into the propulsion performance.

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/microbot3.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/microbot4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

A numerical comparison was conducted between rectangular and circular appendage geometries to determine the optimal shape for propulsion efficiency. Each geometry was subjected to identical magnetic actuation conditions, and performance was evaluated using three criteria: propulsion force generation, deformation stability, and energy efficiency. Results indicated that the circular geometry achieved superior propulsion characteristics, confirming its suitability for microscale swimming applications.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/microbot1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/microbot2.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Presentation Video</h2>

<div class="featured-video">
    <div>
        {% include video.liquid path="https://drive.google.com/file/d/1-kofj6jrM-OoUheTokwfASN0sIvn3w6j/preview" class="img-fluid rounded z-depth-1" title="Microrobotic Systems Presentation" %}
    </div>
</div>


