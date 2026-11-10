---
layout: page
title: PresToe — A Humanoid Robot with Actuated Toes
description: "Co-actuated humanoid hardware, integrated sensing, and whole-body control."
img: assets/img/pres0.jpg
importance: 1
category: work
related_publications: false
featured: true
blurb: "A 23-DoF humanoid with co-actuated legs and articulated toes."
---

<style>
.prestoe-page .equal-height-img { height: 220px; width: 100%; object-fit: contain; background: #fafafa; border-radius: 8px; padding: 4px; }
.prestoe-page .video-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(min(100%, 250px), 1fr)); gap: 1.5rem; margin: 1.5rem 0; }
.prestoe-page .video-grid figure { margin: 0; }
.prestoe-page video { width: 100%; height: 320px; object-fit: contain; background: #111; border-radius: 8px; }
.prestoe-page figcaption { margin-top: .65rem; font-size: .9rem; }
</style>

<div class="prestoe-page" markdown="1">

## From biomechanics to humanoid hardware

PresToe is a human-scale humanoid that brings co-actuation and articulated toes to a complete robot. Building on StaccaToe, its coupled leg transmission allows several actuators to contribute to a joint's motion, taking inspiration from human muscle coordination. The platform combines mechanical design, custom electronics, joint sensing, and whole-body control.

At approximately **1.32 m tall and 32 kg**, PresToe has **23 actuated degrees of freedom**: seven in each leg, four in each arm, and one at the waist. Each leg includes hip yaw, roll, and pitch; knee pitch; ankle pitch and roll; and an actuated toe.

## Mechanical design

The leg combines belt drives and closed-chain linkages to coordinate knee, ankle, and toe motion. Co-actuation lets multiple motors share joint loads, while the articulated toe provides an additional contact and push-off degree of freedom.

- **Belt transmission:** tensioner/idler pulley diameter increased from 17 mm to 30 mm. The revised design has an estimated 48% reduction in belt-bending loss, a design estimate rather than a measured whole-robot energy saving.
- **Experimentally selected belts:** Instron testing guided the selection of 12 mm-wide EV5GT belts. Ankle and toe belt stiffness increased by 26.6% and 14.8%, respectively; the knee achieved similar stiffness with a narrower belt, reduced from 15 mm to 12 mm.
- **Control-aware structural design:** trajectory optimization of 2 m/s running and leaping supplied peak foot loads of approximately 1 kN for structural analysis. All links were designed for a safety factor of at least two. Running and leaping were design simulations.

<div class="row">
  <div class="col-sm-6">{% include figure.liquid path="assets/img/pres1.jpg" alt="PresToe mechanical design" class="equal-height-img" %}</div>
  <div class="col-sm-3">{% include figure.liquid path="assets/img/pres2.png" alt="PresToe leg structure" class="equal-height-img" %}</div>
  <div class="col-sm-3">{% include figure.liquid path="assets/img/pres3.png" alt="PresToe transmission design" class="equal-height-img" %}</div>
</div>

## Electronics, sensing, and communication

I designed and implemented the electronics layout, wiring, power distribution, and communication hierarchy. The torso integrates an UP Xtreme control computer, a Jetson AGX Orin for additional processing, a VN-100 IMU, an event camera, a RealSense depth camera, and two 24 V batteries.

The custom communication board uses **three Teensy 4.1 microcontrollers**, each with Ethernet and three CAN interfaces. Ethernet UDP connects the control computer to the CAN 2.0 actuator network, with two actuators per bus. Mean communication latency is **855 µs**, corresponding to approximately **1.2 kHz**, compared with StaccaToe's 500 Hz link.

Custom encoder boards measure the distal joints directly: 10-bit MA3 encoders at the toe and ankle roll, and a 15-bit TLE5012 sensor at ankle pitch. An AT90CAN128 microcontroller reads all three joints and reports over CAN, providing joint feedback alongside the motor encoders.

<div class="row">
  <div class="col-sm">{% include figure.liquid path="assets/img/pres4.jpg" alt="PresToe custom electronics" class="equal-height-img" %}</div>
  <div class="col-sm">{% include figure.liquid path="assets/img/pres5.jpg" alt="PresToe electronics integration" class="equal-height-img" %}</div>
  <div class="col-sm">{% include figure.liquid path="assets/img/pres6.png" alt="PresToe sensing and communication hardware" class="equal-height-img" %}</div>
</div>

## Control architecture

Whole-body controllers and learned policies share a robot control interface. An impedance regulator connects joint-level commands to the coupled actuators, using motor and joint feedback. Fast local feedback remains on the motor boards.

<figure>
  <a href="{{ '/assets/img/prestoe-impedance-architecture.png' | relative_url }}">
    <img src="{{ '/assets/img/prestoe-impedance-architecture.png' | relative_url }}" alt="Impedance regulator architecture showing joint reference mapping, host-side regulation, motor-board feedback, and sensing for the coupled leg." loading="lazy" style="width: 100%; height: auto; background: white; border-radius: 8px;">
  </a>
  <figcaption>Joint-space impedance regulator architecture. Select the diagram to view it at full resolution.</figcaption>
</figure>

State feedback closes the loop between the robot and the control stack. Hardware demonstrations include whole-body-control squatting, toe-supported balance, and an RL standing policy.

<div class="video-grid">
{% assign balance_clips = 'wbc-squat|Whole-body-control squat,toe-stand|Whole-body-control toe stand,rl-stand|RL standing' | split: ',' %}
{% for clip in balance_clips %}
{% assign details = clip | split: '|' %}
  <figure>
    <video controls playsinline preload="none" poster="{{ '/assets/video/prestoe/' | append: details[0] | append: '.png' | relative_url }}" aria-label="{{ details[1] }}">
      <source src="{{ '/assets/video/prestoe/' | append: details[0] | append: '.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/assets/video/prestoe/' | append: details[0] | append: '.mp4' | relative_url }}">Download {{ details[1] }}</a>.
    </video>
    <figcaption>{{ details[1] }} on PresToe hardware.</figcaption>
  </figure>
{% endfor %}
</div>

## Learning-based locomotion

Velocity-tracking and motion-tracking policies use a shared **mjlab + RSL-RL** training pipeline, with parallel simulation in MuJoCo Warp and PPO training. Training varies dynamics, observation noise, and disturbances. Exported policies run on PresToe through the same control interface.

Hardware experiments demonstrate walking and turning with velocity-tracking policies, and moonwalking with a motion-tracking policy.

<div class="video-grid">
{% assign locomotion_clips = 'walking|Walking — velocity tracking,turning|Turning — velocity tracking,moonwalking|Moonwalking — motion tracking' | split: ',' %}
{% for clip in locomotion_clips %}
{% assign details = clip | split: '|' %}
  <figure>
    <video controls playsinline preload="none" poster="{{ '/assets/video/prestoe/' | append: details[0] | append: '.png' | relative_url }}" aria-label="{{ details[1] }}">
      <source src="{{ '/assets/video/prestoe/' | append: details[0] | append: '.mp4' | relative_url }}" type="video/mp4">
      <a href="{{ '/assets/video/prestoe/' | append: details[0] | append: '.mp4' | relative_url }}">Download {{ details[1] }}</a>.
    </video>
    <figcaption>{{ details[1] }}.</figcaption>
  </figure>
{% endfor %}
</div>

</div>
