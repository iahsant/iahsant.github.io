---
layout: page
title: research
permalink: /projects/
description:
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->

<p>My research develops methods for <b>soft bodies that operate underwater</b>. Soft actuators are compliant and safe around delicate objects, but the surrounding water loads, deforms and damps them in ways that structural models ignore. I work across the pipeline, from designing actuators with fully coupled fluid–structure interaction, to predicting how continuum bodies move over long horizons, to sensing objects before contact when vision fails.</p>

<h4 class="mt-4">Research Areas</h4>
<ul>
  <li>Soft robotics</li>
  <li>Underwater robotics</li>
  <li>Fluid–structure interaction</li>
  <li>Modeling and learning for continuum robots</li>
  <li>Bio-inspired sensing</li>
</ul>

<h4 class="mt-4">Research Focus</h4>

<div class="card mt-3 mb-4">
  <div class="row no-gutters">
    <div class="col-md-4 p-3 d-flex align-items-center">
      <img src="{{ '/assets/img/publication_preview/tmech_fsi.png' | relative_url }}" class="img-fluid rounded" alt="FSI-optimized soft gripper underwater">
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">Designing soft actuators for water</h5>
        <p class="card-text">Soft fluidic actuators are usually designed with structural FEM, which neglects the fluid loading acting on them underwater. I built a <b>two-way external fluid–structure interaction (FSI)</b> optimization framework that trains <b>non-parametric regression surrogates</b> on a design-of-experiments dataset and searches a parameterized geometry space. The FSI optimum reaches similar bending at <b>30% lower pressure</b> than the FEM optimum while bending <b>46% more</b>. In system tests it gives a <b>58% higher retention force</b> in grasping and <b>24.8% faster swimming</b> in a fish-like body.</p>
        <p class="card-text mb-1"><b>Related publications</b></p>
        <p class="card-text small">
          <span class="badge badge-success">Accepted</span>
          A. Tanveer et al., <i>An Optimization Framework for Soft Fluidic Actuators: Fully Coupled FSI Simulation with Surrogate Modeling</i>, IEEE/ASME Transactions on Mechatronics, 2026.
          <a href="{{ '/assets/pdf/Tanveer_TMECH2026_accepted_with_supplementary.pdf' | relative_url }}">[PDF]</a>
          <a href="{{ '/assets/video/tmech_fsi_video.mp4' | relative_url }}">[Video]</a>
          <a href="https://doi.org/10.1109/TMECH.2026.3748317">[DOI]</a>
        </p>
      </div>
    </div>
  </div>
</div>

<div class="card mb-4">
  <div class="row no-gutters">
    <div class="col-md-4 p-3 d-flex align-items-center">
      <img src="{{ '/assets/img/publication_preview/graphicaAbstract.png' | relative_url }}" class="img-fluid rounded" alt="Equilibrium-anchored rollouts for a continuum arm">
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">Predicting continuum robot motion</h5>
        <p class="card-text">Multi-step prediction for continuum robots breaks down under actuation distribution shift, where errors accumulate and rollouts drift or diverge. I proposed a hybrid model that <b>anchors predictions to a learned equilibrium prior</b> through a contractive update and learns the remaining one-step mismatch with a <b>feature-lifted residual model</b> that is linear in parameters. On 200-step rollouts of a tendon-driven 3D continuum arm under stronger and faster actuation than in training, it reduces <b>backbone RMSE by 26% and tip RMSE by 27%</b> and stays stable on every tested trajectory. A soft-tail hardware test confirms the gain under actuation-frequency shift.</p>
        <p class="card-text mb-1"><b>Related publications</b></p>
        <p class="card-text small">
          <span class="badge badge-success">Published</span>
          A. Tanveer et al., <i>Stabilizing 3D Continuum-Arm Rollouts via Equilibrium Anchoring and Feature-Lifted Residual Learning</i>, Robotics: Science and Systems (RSS), 2026.
          <a href="https://www.roboticsproceedings.org/rss22/p106.pdf">[PDF]</a>
          <a href="https://anchored-rollouts.github.io/">[Project page]</a>
          <a href="https://www.youtube.com/watch?v=hs2zDyGOs9k">[Video]</a>
          <a href="https://doi.org/10.15607/RSS.2026.XXII.106">[DOI]</a>
        </p>
      </div>
    </div>
  </div>
</div>

<div class="card mb-4">
  <div class="row no-gutters">
    <div class="col-md-4 p-3 d-flex align-items-center">
      <img src="{{ '/assets/img/publication_preview/exp.png' | relative_url }}" class="img-fluid rounded" alt="Active electrosense on an underwater soft gripper">
    </div>
    <div class="col-md-8">
      <div class="card-body">
        <h5 class="card-title">Sensing before contact underwater</h5>
        <p class="card-text">Turbidity, glare and gripper occlusion make vision unreliable during underwater grasping, and soft grippers usually have no cue before contact. I instrument an octopus-inspired soft gripper with <b>active electrosense</b>, a discrete electrode layout that measures perturbations of an applied electric field in water. Simulation and tank experiments with a conductive sphere show <b>structured, object-dependent changes</b> in the multi-electrode voltage readout across excitations of 5 to 20 V and frequencies from 1 mHz to 1 kHz. This gives a <b>pre-contact cue</b> for guiding approach and closure when vision fails.</p>
        <p class="card-text mb-1"><b>Related publications</b></p>
        <p class="card-text small">
          <span class="badge badge-info">Workshop</span>
          A. Tanveer et al., <i>Toward Gripper-Integrated Active Electrosense for Pre-Contact Sensing in Underwater Soft Grippers</i>, ICRA 2026 Workshop on Manipulation Robustness.
          <a href="{{ '/assets/pdf/electrosense.pdf' | relative_url }}">[PDF]</a>
          <a href="https://openreview.net/forum?id=rdWW5xPrhN">[OpenReview]</a>
          <a href="https://doi.org/10.48550/arXiv.2606.03204">[arXiv]</a>
        </p>
      </div>
    </div>
  </div>
</div>

<h4 class="mt-4">Other Projects</h4>
<div class="projects">
  {% assign other_projects = site.projects | where: "category", "research" | sort: "importance" %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in other_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
</div>
