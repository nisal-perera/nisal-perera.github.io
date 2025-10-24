---
layout: page
title: Design of a Track-Leg Hybrid Locomotive Mobile Robot
description: 
img: assets/img/track_3.jpg
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

Exploration of surface mining sites and other hazardous environments can be an extremely difficult task for a human being. Furthermore, EOD and other first responder situations pose life risks to the trained personnel. Therefore, researchers have been looking into the use of field robotics in these areas. In modern day we can observe various robots being used in this context, especially for EOD. 

In order for a mobile robot to perform in an aforementioned scenario it should have sufficient mobility and dexterity. This project proposes a track-leg hybrid locomotive mobile robot with a 3 DOF robotic arm. The hybrid locomotion consists of a tracked locomotion mode and a legged locomotion mode, enabling the robot to have a higher mobility. The 3 DOF robotic manipulator which is mounted on the platform allows the robot to perform pick and place tasks, sample collection and inspection tasks. A storing chamber is designed in the upper portion of the robot to transport collected mineral samples etc.

<h3><u>Aim</u></h3>
Increasing the use of field robots in Sri Lanka for first responder situations and mining operations.

<h3><u>Objectives</u></h3>
-To design a mobile platform with high mobility and a 3 DOF robotic manipulator.
-To propose a design framework for a track-leg mobile robot.

<h2>Mobile Platform Design</h2>

The mobile platform has four track-leg units to facilitate locomotion. The main components of a track-leg unit are sprockets, a track-arm and a track belt. A coaxial shaft configuration allows relative motion between the sprockets and track-arm, enabling hybrid locomotion. The hip joint is actuated by a direct drive motor during legged locomotion. Two motors transmits power to the track belts through a pair of chain drives. In this power transmission methodology each track-leg can be controlled independently during legged locomotion. Furthermore, a skid steering control strategy can be easily implemented for tracked locomotion. 

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/track_1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/track_2.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/track_3.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>3 DOF Robotic Manipulator</h2>

The 3 DOF serial robotic manipulator was designed for pick and placing tasks, inspection tasks and sample collecting. It can manipulate a maximum payload of 1kg. The manipulator is mounted at the front of the robot and can be easily detached. The end effector is a gripper with two fingers. A finite state machine was developed using simulink/simscape for the operation of the manipulator.

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/track_4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/track_5.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>
