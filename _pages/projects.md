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

<style>
.research-card .card-title { font-weight: 600; }
.research-pub { border-top: 1px solid var(--global-divider-color); padding-top: .6rem; margin-top: .4rem; font-size: .85rem; }
.research-venue { font-weight: 600; color: var(--global-theme-color); margin-right: .5rem; }
.research-status { font-size: .7rem; text-transform: uppercase; letter-spacing: .04em; border: 1px solid var(--global-text-color-light); color: var(--global-text-color-light); border-radius: 1rem; padding: .05rem .5rem; }
.research-paper { font-style: italic; margin: .35rem 0 .5rem; }
.research-links a { display: inline-block; font-size: .75rem; border: 1px solid var(--global-text-color); color: var(--global-text-color); border-radius: .25rem; padding: .1rem .55rem; margin: 0 .3rem .3rem 0; text-decoration: none; }
.research-links a:hover { border-color: var(--global-theme-color); color: var(--global-theme-color); }
</style>

<p>My research addresses the design, modeling, and sensing of <b>soft robotic systems operating underwater</b>. Hydrodynamic loading alters the deformation, energetics, and stability of soft bodies in ways that structural models and in-air assumptions fail to capture. My work spans fluid–structure interaction-based design optimization of soft actuators, stable long-horizon prediction for continuum robots, and pre-contact sensing for underwater soft manipulation.</p>

<h4 class="mt-4">Research Areas</h4>
<ul>
  <li>Soft robotics</li>
  <li>Underwater robotics</li>
  <li>Fluid–structure interaction</li>
  <li>Modeling and learning for continuum robots</li>
  <li>Bio-inspired sensing</li>
</ul>

<h4 class="mt-4">Research Focus</h4>

<div class="card research-card mb-4">
  <div class="row no-gutters">
    <div class="col-md-5 p-3 d-flex align-items-center">
      <video class="img-fluid rounded" autoplay loop muted playsinline preload="metadata"><source src="{{ '/assets/video/tmech_research_clip.mp4' | relative_url }}" type="video/mp4"></video>
    </div>
    <div class="col-md-7">
      <div class="card-body">
        <h5 class="card-title">Fluid–Structure Interaction-Based Design of Soft Actuators</h5>
        <p class="card-text">Structural finite element analysis, the standard tool for designing soft fluidic actuators (SFAs), neglects the hydrodynamic loads acting on the actuator underwater and therefore biases the predicted pressure–deformation response. We present a geometric optimization framework that places <b>two-way external fluid–structure interaction (FSI)</b> simulation inside the design loop. <b>Non-parametric regression (NPR) surrogates</b> trained on a design-of-experiments dataset are searched over a parameterized design space, and the resulting optimum is verified with high-fidelity coupled simulation. The FSI-optimized actuator reaches comparable bending at <b>30% lower pressure</b> than the FEM-optimized design while increasing the bending angle by <b>46%</b>. System-level tests report a <b>58% higher retention force</b> in grasping and a <b>24.8% higher forward velocity</b> in a fish-like swimmer.</p>
        <div class="research-pub">
          <span class="research-venue">IEEE/ASME T-MECH 2026</span><span class="research-status">Accepted</span>
          <div class="research-paper">An Optimization Framework for Soft Fluidic Actuators: Fully Coupled FSI Simulation with Surrogate Modeling</div>
          <div class="research-links"><a href="{{ '/assets/pdf/Tanveer_TMECH2026_accepted_with_supplementary.pdf' | relative_url }}">PDF</a><a href="{{ '/assets/video/tmech_fsi_video.mp4' | relative_url }}">Video</a><a href="https://doi.org/10.1109/TMECH.2026.3748317">DOI</a></div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="card research-card mb-4">
  <div class="row no-gutters">
    <div class="col-md-5 p-3 d-flex align-items-center">
      <img src="{{ '/assets/img/research/rss_framework.png' | relative_url }}" class="img-fluid rounded" alt="Hybrid equilibrium-anchored residual learning framework">
    </div>
    <div class="col-md-7">
      <div class="card-body">
        <h5 class="card-title">Stable Long-Horizon Prediction for Continuum Robots</h5>
        <p class="card-text">Multi-step motion prediction for continuum robots suffers from error accumulation under actuation distribution shift, which distorts the predicted steady-state response and destabilizes rollouts. We propose a hybrid <b>equilibrium-anchored residual-learning</b> framework for a tendon-driven 3D continuum arm. An equilibrium prior learned from static data is enforced through a <b>contractive update</b> that pulls each prediction toward the equilibrium estimate, and a <b>feature-lifted residual model</b>, linear in parameters, recovers the remaining transient dynamics from trajectory data. Over 200-step rollouts under stronger and faster actuation than seen in training, the method reduces backbone and tip position RMSE by <b>26%</b> and <b>27%</b>, respectively, and remains stable on all tested trajectories. A soft-tail hardware experiment under actuation-frequency shift further validates the approach.</p>
        <div class="research-pub">
          <span class="research-venue">RSS 2026</span><span class="research-status">Published</span>
          <div class="research-paper">Stabilizing 3D Continuum-Arm Rollouts via Equilibrium Anchoring and Feature-Lifted Residual Learning</div>
          <div class="research-links"><a href="https://www.roboticsproceedings.org/rss22/p106.pdf">PDF</a><a href="https://anchored-rollouts.github.io/">Project</a><a href="https://www.youtube.com/watch?v=hs2zDyGOs9k">Video</a><a href="https://doi.org/10.15607/RSS.2026.XXII.106">DOI</a></div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="card research-card mb-4">
  <div class="row no-gutters">
    <div class="col-md-5 p-3 d-flex align-items-center">
      <img src="{{ '/assets/img/research/electrosense_fig1.png' | relative_url }}" class="img-fluid rounded" alt="Electrode layout and simulated electric field of the electrosensing gripper">
    </div>
    <div class="col-md-7">
      <div class="card-body">
        <h5 class="card-title">Pre-Contact Electrosensing for Underwater Soft Grippers</h5>
        <p class="card-text">Vision-based perception degrades during underwater manipulation because of turbidity, glare, and occlusion by the gripper itself, and soft grippers generally lack an onboard cue prior to contact. This work investigates <b>active electrosense</b> as a pre-contact sensing modality for underwater soft grippers. An octopus-inspired gripper is instrumented with a <b>discrete electrode layout</b>, and perturbations of an applied electric field are recorded as multi-channel sensing voltages. Simulation and tank experiments with a suspended conductive sphere show <b>structured, object-dependent voltage changes</b> relative to empty-water baselines for excitation amplitudes of 5–20 V and frequencies from 1 mHz to 1 kHz.</p>
        <div class="research-pub">
          <span class="research-venue">ICRA 2026 Workshop</span><span class="research-status">Workshop paper</span>
          <div class="research-paper">Toward Gripper-Integrated Active Electrosense for Pre-Contact Sensing in Underwater Soft Grippers</div>
          <div class="research-links"><a href="{{ '/assets/pdf/electrosense.pdf' | relative_url }}">PDF</a><a href="https://openreview.net/forum?id=rdWW5xPrhN">OpenReview</a><a href="https://arxiv.org/abs/2606.03204">arXiv</a></div>
        </div>
      </div>
    </div>
  </div>
</div>

<h4 class="mt-4">Current Work</h4>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">Actuator-Effectiveness Estimation for Policy Recovery</h5>
    <p class="card-text">Actuator loss of effectiveness breaks the action-to-motion map assumed by learned robot policies, yet the fault is rarely measured directly at deployment. This work introduces an explicit <b>diagnosis–recovery interface</b> in which a trajectory-level identifier estimates a continuous actuator-effectiveness factor from recent observation–action history, and a task-specific recovery module acts on this estimate while the nominal policy remains frozen. On tendon-driven continuum robot reaching, <b>fault-conditioned MPC</b> reduces terminal error by up to <b>38.0%</b>, and on locomotion benchmarks diagnosis-conditioned residual policies improve return by up to <b>53.6%</b>.</p>
    <div class="research-pub">
      <span class="research-venue">Journal article</span><span class="research-status">Under review</span>
      <div class="research-paper">Explicit Actuator-Effectiveness Estimation for Post-Training Robot Policy Recovery</div>
      
    </div>
  </div>
</div>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">World Models for Robot Swarms</h5>
    <p class="card-text">This project develops a <b>world model</b> for swarms of camera-equipped Raspberry Pi differential-drive robots, building on onboard neighbor position estimation. The model is implemented as a <b>spiking neural network</b> compact enough to run on every robot and serves as the basis for decentralized control.</p>
    <div class="research-pub">
      <span class="research-venue">MPI of Animal Behavior</span><span class="research-status">Ongoing</span>
      
      
    </div>
  </div>
</div>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">System Identification of Fish Responses to a Virtual Conspecific</h5>
    <p class="card-text">This project models how zebrafish respond to a virtual fish whose heading undergoes step changes from 15° to 180° in both turning directions. Following a <b>stimulus–response system identification</b> approach, it seeks an interpretable model of the turning response that yields biological insight and supports a controller that shapes the virtual fish path so that real fish track it in <b>closed loop</b>.</p>
    <div class="research-pub">
      <span class="research-venue">MPI of Animal Behavior</span><span class="research-status">Ongoing</span>
      
      
    </div>
  </div>
</div>
<h4 class="mt-4">Collaborative Work</h4>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">Proprioception from Energy-Harvesting Transducers</h5>
    <p class="card-text">This work investigates whether <b>piezoelectric transducers</b> embedded in a passive soft hydrofoil for energy harvesting can also provide proprioception without dedicated sensing elements. Using only the embedded PVDF signals, a <b>bidirectional LSTM</b> reconstructs the dynamic midline on held-out flow conditions with <b>0.68 mm RMSE</b> and R² = 0.83.</p>
    <div class="research-pub">
      <span class="research-venue">ICRA 2027</span><span class="research-status">Under review</span>
      <div class="research-paper">The Harvester as Proprioceptor: Midline Pose Estimation of a Passive Soft Foil in Flow</div>
      
    </div>
  </div>
</div>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">Bio-to-Robot Transfer of Fish Sensorimotor Dynamics</h5>
    <p class="card-text">An interpretable <b>ARX system identification</b> approach maps bidirectionally between EMG and kinematics in freely swimming koi across laminar, Kármán vortex, and reverse Kármán vortex flows, and its generalization is tested on a <b>robotic fish</b>.</p>
    <div class="research-pub">
      <span class="research-venue">Advanced Intelligent Systems 2025</span><span class="research-status">Published</span>
      <div class="research-paper">Bio-to-Robot Transfer of Fish Sensorimotor Dynamics via Interpretable Model</div>
      <div class="research-links"><a href="{{ '/assets/pdf/biorob.pdf' | relative_url }}">PDF</a><a href="https://bio-to-robot.github.io/">Project</a><a href="https://doi.org/10.1002/aisy.202501117">DOI</a></div>
    </div>
  </div>
</div>

<div class="card research-card mb-3">
  <div class="card-body">
    <h5 class="card-title">EMG-Driven Telemetry for Freely Swimming Fish</h5>
    <p class="card-text">A custom <b>16-channel telemetry unit</b> records intramuscular EMG synchronized with kinematics in freely swimming fish, and the resulting framework decodes both <b>body pose</b> and <b>flow conditions</b> from the EMG signals.</p>
    <div class="research-pub">
      <span class="research-venue">Advanced Intelligent Systems 2026</span><span class="research-status">Published</span>
      <div class="research-paper">EMG-Driven Telemetry and Inference System for Fish: Pose Reconstruction and Flow Sensing</div>
      <div class="research-links"><a href="{{ '/assets/pdf/emg.pdf' | relative_url }}">PDF</a><a href="https://emg-fish-kinematics.github.io/">Project</a><a href="https://doi.org/10.1002/aisy.202501085">DOI</a></div>
    </div>
  </div>
</div>
