---
layout: page
title: StaccaToe -- A Single-Leg Robot that Mimics the Human Leg and Toe
description: 
img: assets/img/publication_preview/staccatoe.gif
importance: 2
category: work
related_publications: true
featured: true
blurb: "Human-scale single-leg robot with actuated toe and co-actuated knee for agile locomotion."
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

The StaccaToe project introduces a human-scale, electric-motor-powered single-leg robot aimed at replicating the agility of the human leg and foot. Unlike many prior systems that depend on springs, clutches, hydraulics or pneumatics, StaccaToe uses direct electric actuation without energy-storage mechanisms, marking a step toward practical, high-performance robotics. Two core biomechanical inspirations drive the design: an actuated toe (to enable human-like foot mechanics) and a co-actuation configuration at the knee (to boost force output and agility).

<h2>Robot Design Highlights</h2>
<ul>
<li><b>Actuated Toe Mechanism</b>: Incorporating an actively controlled toe joint enables tip-toe balance control and more nuanced foot interactions, offering improved stability and dynamic motion capabilities.</li> 

<li><b>Co-actuation Configuration</b>: The knee joint is designed so that multiple actuators work cooperatively rather than purely serially, increasing torque generation during extension and push-off phases. </li> 

<li><b>Component & Link Optimization</b>: The thigh and shank modules underwent topology optimization and component count reduction, resulting in a lighter, narrower leg structure with fewer failure points. For example, the lower leg link mass dropped ~14.8% compared to its predecessor.</li> 

<li><b>Power and Control Electronics</b>: A custom power board supports operation at up to 48 V, paired with high-performance motor drivers and CAN-based communication to support real-time control.</li>

</ul>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stac1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stac2.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Control Strategy</h2>

StaccaToe uses a Whole-Body Impulse Control (WBIC) framework for balance and dynamic maneuvers, combined with trajectory optimization via a single-rigid-body dynamics model to generate jumping maneuvers that fully exploit the co-actuation mechanism. Experiments demonstrate the robot maintaining a tip-toe stance and executing dynamic jumps, reflecting both control fidelity and hardware synergy.

<h2>Contributions</h2>
<ul>
<li><b>First human-scale, electric-motor-driven single-leg robot</b> capable of dynamic maneuvers (balance, jump) without relying on specialized mechanical energy-storage devices.</li> 

<li><b>Empirical validation of biomechanical leg features:</b> The study provides evidence that incorporating actuated toe mechanisms and co-actuation improves agility and control — insights that are rare in existing literature. </li>

<li><b>Comprehensive documentation of design & control:</b> The paper details link optimization, actuator identification, cable management, power electronics design, and controller implementation — providing a concrete roadmap for agile legged robot development. </li>
</ul>

<div class="row">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stac3.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/stac4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<div style="text-align:center; margin: 20px 0;">
  <iframe width="640" height="360" 
          src="https://www.youtube.com/watch?v=jZwrF528Fg0" 
          title="StaccaToe Demo" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
  </iframe>
</div>