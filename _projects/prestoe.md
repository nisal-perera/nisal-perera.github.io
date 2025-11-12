---
layout: page
title: Prestoe -- A Humanoid Robot with Actuated Toe
description: 
img: assets/img/pres0.jpg
importance: 1
category: work
related_publications: false
featured: true
blurb: "Humanoid robot with actuated toes for energy efficient locomotion."
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

PresToe is a human-scale humanoid robot designed to extend the biomechanical innovations first introduced in StaccaToe — namely, co-actuated joints and an actuated toe mechanism to explore energy efficient humanoid locomotion. Standing approximately 1.32 m tall and weighing around 31–32 kg, PresToe features 23 actuated degrees of freedom, with electrically powered joints throughout. It represents a major step toward human-like legged locomotion that combines biomechanical fidelity, control robustness, and full-body coordination. The project advances toward whole-body dynamic behaviors such as running, leaping, and balancing, powered entirely by onboard computation and energy systems.
 

<h2>Robot Design Highlights</h2>
PresToe’s leg employs a 7-DOF configuration per leg, inspired by human joint synergy. The robot adopts co-actuation and actuated toe mechanisms refined from StaccaToe. The crossed four-bar and spatial six-bar linkages map motor space to joint space, enabling torque amplification at critical motion phases. Co-actuation between knee and ankle allows dynamic force sharing during stance and push-off, improving energy efficiency and torque output.

The robot adopts co-actuation and actuated toe mechanisms refined from StaccaToe:

<li>The crossed four-bar and spatial six-bar linkages map motor space to joint space, enabling torque amplification at critical motion phases.</li>
<li>Co-actuation between knee and ankle allows dynamic force sharing during stance and push-off, improving energy efficiency and torque output.</li>

<b>Structural and Transmission Design:</b> PresToe’s structural components were designed through finite element analysis (FEA) and topology optimization, guided by control-aware design principles. The mechanical layout and load paths were informed by optimal control simulation results, ensuring that the leg structure can withstand forces generated during dynamic motions such as running at 2 m/s and leaping maneuvers. This co-design process between control and structure resulted in components with minimum safety factors above 2.0, balancing lightweight construction with robustness. A redesigned belt-drive transmission with larger pulley diameters (30 mm vs 17 mm) reduces hysteresis losses by 48% compared to StaccaToe, minimizing energy dissipation during cyclic bending and improving backdrivability.

High-stiffness EV5GT timing belts (12 mm width, 5 mm pitch) were selected based on experimental tensile testing using an Instron material tester, ensuring consistent torque transfer and minimal compliance in high-load joints.

</ul>
<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres2.png" title="example image" class="equal-height-img z-depth-1" %}
    </div>
     <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres3.png" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Electronics and Motor Control</h2>

A custom 48 V power distribution board was developed to supply all actuators and auxiliary electronics, ensuring reliable high-current delivery while maintaining electrical isolation and protection.

The communication backbone employs three CAN 2.0 buses interfaced through a custom CAN communication board built around Teensy 4.1 microcontrollers, which bridge the actuator network to the onboard computer via Ethernet UDP. This setup achieves an average communication bandwidth of 1.17 kHz, supporting real-time torque and state feedback across all joints.

In addition, custom encoder boards were designed specifically to measure ankle pitch and roll angles, each based on an AT90CAN128 MCU integrated with absolute magnetic encoders (MA3 and TLE5012BE1000). These boards provide direct CAN communication and enable precise joint angle estimation through PWM or SPI interfaces, ensuring accurate low-latency feedback for the robot’s balance-critical joints.

The entire electronics layout, wiring scheme, and communication hierarchy—including the power distribution, CAN buses, and sensor interfacing—were designed and implemented by me.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres5.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/pres6.png" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>
