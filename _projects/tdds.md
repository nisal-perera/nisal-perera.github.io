---
layout: page
title: Design and Analysis of a Transdermal Drug Delivery System
description: 
img: assets/img/proteanbot_real.jpg
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

<h2>Motivation</h2>
Many pharmaceutical drugs used for various diseases have systemic side effects due to sudden fluctuation in the blood level profile. This includes medication such as Insulin (to maintain the blood sugar level) and Levodopa (treatment of Parkinson’s Disease). In addition to this the use of injections using hypodermic needles have their own disadvantages such as the time taken for healing of the damaged skin and also the psychological effect of using hypodermic needles on the patient. Transdermal patches have helped in avoiding these disadvantages. Transdermal drug patches help in diffusing the drug through the skin with a predetermined controlled release rate. The main drawback of this method is that only drugs with small molecular sizes can diffuse through the stratum corneum layer of the skin. 

In the context of treating Parkinson's disease, maintaining a steady concentration of Levodopa within the body is essential. The current pill-based treatment routine causes sudden fluctuations in the Levodopa concentration and is not completely effective in suppressing tremors. 

<h2>Introduction</h2>

MEMS-based transdermal drug delivery systems are a solution to aforementioned problems. With the use of such a system Levodopa can be administrated at a controlled rate for an extended period of time. Here, usually the stratum corneum is penetrated using an array of micro needles thus the barrier of the skin is not present. As the needles have a diameter in the micron range, the damaged cause to the skin is minimum. Micro-pumps can be used to actively supply a steady flow rate of drugs into the blood stream. These systems can be developed as wearable technology.  In addition to the above-mentioned applications of transdermal drug delivery, it can also be used to administrate analgesic medication (pain relief medication) in sports applications such as cramp prevention or in the military as a controlled release supply of adrenaline.

The proposed conceptual design of the transdermal drug delivery system of this project is shown below.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tdds_1.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Design</h2>

A piezoelectric pump was selected as the most suitable pump due to its high stroke volume, high actuation force, high precision, low cost, low power and light weight. An out-of-plane needle design was selected due to their ability to achieve a high density of needles per chip, ability to fabricate on a thin flat plate making it more suitable as a wearable device, better skin penetration without breakage, robustness and reduced transdermal water loss. A 18x18 microneedle array was designed with robust capabilities to penetrate skin and supply Levodopa was designed.

<div class="row justify-content-sm-center">
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tdds_2.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tdds_3.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
     <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tdds_4.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>

<h2>Fluid-Particle Interaction</h2>

The modelling of the drug was conducted as Levodopa molecules (assumed to be spherical particles) suspended in water. The water solubility of Levodopa is 5000 mg/L while the concentration is 1 mg/L. An average dosage of 240 L/h to 840 L⁄h for 8 hours of Levodopa is used for the study. The behavior of the Levodopa particles within the liquid was modeled as fluid-particle interaction.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/tdds_5.jpg" title="example image" class="equal-height-img z-depth-1" %}
    </div>
</div>
