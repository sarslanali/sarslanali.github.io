---
layout: page
title: LaneFreeDrive
permalink: /software/lanefreedrive/
description: Modular C++ control-algorithm library for lane-free traffic, built on TrafficFluid-Sim (modified SUMO).
img: assets/img/projects/LaneFreeDrive/lanefreedrive-pl-controller.jpg
importance: 2
category: software
---

<style>
  .lanefree-page { --pl-width: 48%; --apl-width: 51%; --waves-width: 55%; }
  .lanefree-page h2 { clear: both; }
  .lanefree-figure { float: right; width: var(--figure-width); max-width: 100%; margin: 0.35rem 0 1rem 1.4rem; }
  .lanefree-figure.left { float: left; margin: 0.35rem 1.4rem 1rem 0; }
  .lanefree-figure img { display: block; width: 100%; height: auto; }
  .lanefree-figure figcaption { margin-top: 0.4rem; font-size: 0.75rem; line-height: 1.45; color: var(--global-text-color-light, #666); }
  @media (max-width: 720px) { .lanefree-figure, .lanefree-figure.left { float: none; width: 100%; margin: 1rem 0; } }
</style>

<div class="lanefree-page" markdown="1">

**Research software · Lane-free traffic · Connected autonomous vehicles · C++ / Python · TrafficFluid-Sim / SUMO**

[**GitHub repository**](https://github.com/TUM-VT/LaneFreeDrive) · [**Peer-reviewed paper (2025)**](https://doi.org/10.1016/j.trc.2025.105315)

## Project overview

**LaneFreeDrive** is a modular library of control algorithms and simulation tools for studying **lane-free traffic (LFT)**, in which connected autonomous vehicles (CAVs) coordinate longitudinal and lateral movements without being constrained to fixed lanes. The library brings different control approaches into a common software structure, facilitating implementation, testing and comparison under configurable traffic scenarios.

The framework runs on **TrafficFluid-Sim**, a modified version of the microscopic traffic simulator **SUMO** developed for lane-free traffic. It supports experiments with coordinated CAVs as well as **mixed traffic involving human-driven vehicles (HDVs)**. The 2025 publication demonstrates the framework on a ring road; the library is being extended to other control methods and traffic scenarios.

## Simulation integration and modular design

The core vehicle-control methods are implemented in **C++** through the TrafficFluid-Sim plug-in interface. At each simulation step, the controller accesses vehicle states and supplies longitudinal and lateral acceleration commands. **Python scripts** help generate scenarios, configure experiments and run multiple simulations in parallel.

The software separates control logic from experiment setup using reusable components and **`.ini` configuration files**. Default settings can be overridden for individual scenarios, making it easier to switch algorithms, tune parameters and compare methods without repeatedly editing the simulation code.

## Lane-free control algorithms

<figure class="lanefree-figure" style="--figure-width: var(--pl-width);">
  <a href="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-pl-controller.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size potential fields and potential lines controller diagram">
    <img src="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-pl-controller.jpg' | relative_url }}" alt="Potential fields, artificial forces and the Potential Lines controller for lane-free traffic" loading="lazy">
  </a>
  <figcaption>Figure 3. Potential fields, artificial forces and the Potential Lines controller. <a href="https://doi.org/10.1016/j.trc.2025.105315">source</a> (CC BY 4.0).</figcaption>
</figure>

One implemented approach is the **Potential Lines (PL) controller**, which organizes CAVs laterally according to their desired speeds while using artificial repulsive and nudging forces to coordinate surrounding vehicles. The published implementation also incorporates **safe-velocity constraints** to reduce collision risks in dense or mixed traffic.

To study the transition from fully connected to mixed traffic, LaneFreeDrive also incorporates a **strip-based human-driver model** that allows continuous lateral movements. CAVs can coordinate their own movements, while HDVs are modeled as non-connected vehicles that do not respond to artificial CAV control forces.

## Adaptive control for mixed traffic

<figure class="lanefree-figure left" style="--figure-width: var(--apl-width);">
  <a href="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-apl-corridors.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size adaptive potential line corridors diagram">
    <img src="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-apl-corridors.jpg' | relative_url }}" alt="Adaptive Potential Lines corridors formed around human-driven vehicles" loading="lazy">
  </a>
  <figcaption>Figure 4. Adaptive Potential Lines corridors around HDVs. <a href="https://doi.org/10.1016/j.trc.2025.105315">source</a> (CC BY 4.0).</figcaption>
</figure>

The **Adaptive Potential Lines (APL)** controller was developed to reduce the restrictions that HDVs impose on CAV movements. It modifies the lateral PL positions near HDVs and creates **APL corridors** that can help CAVs overtake slower vehicles while maintaining coordinated movement.

The publication evaluates four APL variants with different corridor-activation rules: **Constant Margin (CM)**, **Neighboring Speed-based Constant Margin (NSCM)**, **Follower-based Adaptive Margin (FAM)**, and **Safe Velocity-based Adaptive Margin (SVAM)**. This illustrates how the library can be used to test alternative control strategies within a shared microscopic simulation setup.

## My contributions

At the Technical University of Munich, I developed LaneFreeDrive as a more modular, configurable research framework. My contributions include:

- Redesigning the base TrafficFluidSim plugin with **reusable control components**.
- Replacing hard-coded control parameters with **configuration-driven experiment settings**.
- Adding **human-driven vehicle behavior** for mixed CAV–HDV simulations.
- Developing and evaluating **safe-velocity modifications** and the **Adaptive Potential Lines** control approach.
- Supporting systematic simulation experiments and comparative analysis of control strategies.

## Example application: mixed lane-free traffic

<figure class="lanefree-figure" style="--figure-width: var(--waves-width);">
  <a href="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-traffic-waves.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size spatio-temporal traffic speed plots">
    <img src="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-traffic-waves.jpg' | relative_url }}" alt="Spatio-temporal vehicle speed plots showing traffic waves for increasing HDV percentages" loading="lazy">
  </a>
  <figcaption>Figure 8. Traffic waves arising as HDV penetration increases under the PL controller. <a href="https://doi.org/10.1016/j.trc.2025.105315">source</a> (CC BY 4.0).</figcaption>
</figure>

In our [2025 study](https://doi.org/10.1016/j.trc.2025.105315), LaneFreeDrive was used to compare CAV-only and mixed CAV–HDV traffic on a **1 km ring road**. The simulations showed that introducing just **5% HDVs reduced maximum traffic flow by about 20%** relative to the all-CAV case. APL strategies improved performance over the baseline PL controller, with a peak average flow improvement of **nearly 10%** in the evaluated conditions.

These are **scenario-specific simulation findings**, not predictions for every road network. The ring-road configuration and chosen controller models may influence how strongly traffic disruptions appear.

## Ongoing development

LaneFreeDrive is being extended along three research directions:

- **Reinforcement learning:** learning-based control methods for adapting CAV coordination to different traffic conditions.
- **Vehicle flocking:** investigating group-level coordination and flocking behavior in lane-free traffic.
- **Mixed traffic at ramps:** examining CAV–HDV interactions in merging and ramp scenarios beyond the published ring-road setting.

*These extensions are in progress and are not presented as results of the 2025 publication.*

## Code and publication

- **Repository:** [TUM-VT/LaneFreeDrive](https://github.com/TUM-VT/LaneFreeDrive)
- **Simulation engine:** [TrafficFluid-Sim (TU Crete)](https://www.trafficfluid.tuc.gr/en/trafficfluid-sim)
- **Publication:** Syed, A. A., Rostami-Shahrbabaki, M., & Bogenberger, K. (2025). *Can human drivers and connected autonomous vehicles co-exist in lane-free traffic? A microscopic simulation perspective.* Transportation Research Part C, **180**, 105315. [DOI: 10.1016/j.trc.2025.105315](https://doi.org/10.1016/j.trc.2025.105315)

<small>**Image credits:** Figures 3, 4 and 8 extracted from Syed et al. (2025) and reproduced under <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>. All figures can be opened at full resolution.</small>

</div>
