---
layout: page
title: Research Areas & Expertise
permalink: /research/
description:
nav: true
nav_order: 1
---

<style>
.research-page h2 { font-size: 1.5rem; margin: 2.25rem 0 1rem; }
.research-page .research-intro { line-height: 1.7; max-width: 78ch; }
.research-expertise-grid { display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 0.85rem; margin: 1.1rem 0 2rem; }
.research-expertise-card { background: var(--global-card-bg-color); border: 1px solid var(--global-divider-color); border-radius: 8px; padding: 1rem 1.1rem; }
.research-expertise-card strong { display: block; font-size: 0.95rem; font-weight: 600; margin-bottom: 0.35rem; }
.research-expertise-card span { display: block; font-size: 0.85rem; line-height: 1.7; color: var(--global-text-color); }
.research-area { border-top: 1px solid var(--global-divider-color); padding: 1.35rem 0 0.85rem; }
.research-area h3 { clear: both; font-size: 1.24rem; font-weight: 600; margin: 0 0 0.7rem; }
.research-area p, .research-area li { line-height: 1.65; }
.research-area ul { margin-top: 0.35rem; margin-bottom: 0.9rem; }
.research-area-figure { float: right; width: 50%; max-width: 100%; margin: 0.35rem 0 1rem 1.5rem; }
.research-area-figure img { display: block; width: 100%; height: auto; }
.research-area-figure figcaption { margin-top: 0.4rem; font-size: 0.75rem; line-height: 1.45; color: var(--global-text-color-light, #666); }
.research-area-figure a:focus-visible { outline: 2px solid currentColor; }
.research-area-clear { clear: both; }
@media (max-width: 650px) { .research-expertise-grid { grid-template-columns: 1fr; } .research-area-figure { float: none; width: 100%; margin: 1rem 0; } }
</style>

<div class="research-page" markdown="1">

<p class="research-intro">My research combines mathematical optimization, machine learning, scientific computing, and simulation to develop models and control algorithms for complex systems. My work has primarily focused on transportation and mobility, including fleet optimization, traffic simulation, and connected autonomous vehicles, while the underlying computational methods are applicable across different domains.</p>

## Methodological Expertise

<div class="research-expertise-grid">
  <div class="research-expertise-card"><strong>Optimization & Decision-Making</strong><span>Vehicle–request assignment</span><span>Fleet repositioning</span><span>Routing</span><span>Heuristics and metaheuristics</span></div>
  <div class="research-expertise-card"><strong>Machine Learning & Data-Driven Methods</strong><span>Neural-network-assisted optimization</span><span>Demand forecasting</span><span>Data-driven travel-time modeling</span></div>
  <div class="research-expertise-card"><strong>Simulation & Systems Modeling</strong><span>Agent-based simulation</span><span>Microscopic traffic models</span><span>Scenario design and evaluation</span></div>
  <div class="research-expertise-card"><strong>Scientific Computing & Research Software</strong><span>Python and C++</span><span>Modular simulation architectures</span><span>Reusable computational workflows</span></div>
</div>

For a complete list of publications, see [Publications]({{ '/publications/' | relative_url }}). For implementation details and research software, see [Projects]({{ '/projects/' | relative_url }}).

## Core Research Areas

<section class="research-area" id="mobility-services" markdown="1">

### 01. Mobility Services & Optimization

<figure class="research-area-figure">
  <a href="{{ '/assets/img/research/imbalance_density.png' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/research/imbalance_density.png' | relative_url }}" alt="Reachability-density-based fleet supply-demand imbalance KPI" loading="lazy"></a>
  <figcaption>Reachability-density-based fleet supply-demand imbalance KPI. <a href="https://mediatum.ub.tum.de/1714855">Source</a>.</figcaption>
</figure>

I investigate how shared and on-demand mobility services can be operated efficiently. My contributions include methods for **dynamic ride-request assignment, fleet repositioning, learning-assisted optimization, and electric-vehicle charging strategies**. I have also developed fleet-control methods for integrating passenger transport with last-mile parcel deliveries.

<div class="research-area-clear"></div>

**Selected publications**

- [Density Based Distribution Model for Repositioning Strategies of Ride Hailing Services](https://doi.org/10.3389/ffutr.2021.681451) (2021)
- [Neural Network-Based Metaheuristic Parameterization for Vehicle Matching](https://doi.org/10.1177/0361198119846099) (2019)
- [Asynchronous Adaptive Large Neighborhood Search for Dynamic Ride-Hailing Matching](https://doi.org/10.1109/ITSC.2019.8916943) (2019)
- [Charge Point Search Policies for EVs](https://doi.org/10.1109/ITSC55140.2022.9921802) (2022)

**Related software and projects:** [FleetPy]({{ '/software/fleetpy/' | relative_url }}) · [CONDUCTOR]({{ '/projects/conductor/' | relative_url }}) · [München elektrisiert]({{ '/projects/muenchen-elektrisiert/' | relative_url }}) · [BMW patent applications]({{ '/patents/' | relative_url }})

</section>

<section class="research-area" id="simulation-modeling" markdown="1">

### 02. Simulation Frameworks

<figure class="research-area-figure">
  <a href="{{ '/assets/img/research/fleetpy.png' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/research/fleetpy.png' | relative_url }}" alt="Configuration inputs for FleetPy simulations" loading="lazy"></a>
  <figcaption>Configurable inputs for FleetPy simulations. <a href="https://doi.org/10.1186/s12544-026-00823-3">Source</a> (<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>).</figcaption>
</figure>

A central part of my work is building **modular simulation frameworks** for the analysis of complex mobility systems. As a founding co-developer of **FleetPy**, I contributed to an open-source platform for mobility-on-demand research. I also developed **LaneFreeDrive**, a reusable library for testing lane-free traffic control methods. My modeling work includes data-driven representation of travel times and reproducible simulation-based comparisons.

<div class="research-area-clear"></div>

**Selected publications**

- [FleetPy: An Open Source Simulator for Reproducible Research on Mobility-on-Demand Services](https://doi.org/10.1186/s12544-026-00823-3) (2026)
- [Data-Driven Spatio-Temporal Scaling of Travel Times for AMoD Simulations](https://doi.org/10.1109/ITSC57777.2023.10422313) (2023)

**Related software:** [FleetPy]({{ '/software/fleetpy/' | relative_url }}) · [LaneFreeDrive]({{ '/software/lanefreedrive/' | relative_url }})

</section>

<section class="research-area" id="autonomous-traffic" markdown="1">

### 03. Connected & Autonomous Traffic Systems

<figure class="research-area-figure">
  <a href="{{ '/assets/img/research/lanefreedrive-apl-corridors.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/research/lanefreedrive-apl-corridors.jpg' | relative_url }}" alt="Adaptive Potential Lines corridors around human-driven vehicles" loading="lazy"></a>
  <figcaption>Adaptive Potential Lines corridors around HDVs. <a href="https://doi.org/10.1016/j.trc.2025.105315">Source</a> (CC BY 4.0).</figcaption>
</figure>

I study traffic systems in which **connected autonomous vehicles (CAVs) and human-driven vehicles** interact. My recent research examines the performance of lane-free traffic under mixed vehicle populations using microscopic simulation. I have also contributed to the conceptual design of driving-simulator studies investigating human experience and interaction in lane-free traffic scenarios.

<div class="research-area-clear"></div>

**Selected publications**

- [Can Human Drivers and Connected Autonomous Vehicles Co-exist in Lane-Free Traffic?](https://doi.org/10.1016/j.trc.2025.105315) (2025)
- [Investigating Lane-Free Traffic with a Dynamic Driving Simulator](https://doi.org/10.1109/ITSC57777.2023.10421947) (2023)
- [Lane-Free Traffic: History and State of the Art](https://doi.org/10.1109/ITSC55140.2022.9922282) (2022)

**Related software and projects:** [LaneFreeDrive]({{ '/software/lanefreedrive/' | relative_url }}) · [SAVeNoW]({{ '/projects/savenow/' | relative_url }})

</section>

<section class="research-area" id="adaptive-digital-twins" markdown="1">

### 04. Adaptive Mobility Digital Twins & Agentic AI

<figure class="research-area-figure" style="width: 35%;">
  <a href="{{ '/assets/img/research/adaptive_digital_twins.png' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/research/adaptive_digital_twins.png' | relative_url }}" alt="Growing gap between mobility digital twins and reality over time" loading="lazy"></a>
  <figcaption>Growing gap between mobility digital twins and reality over time.</figcaption>
</figure>

I am interested in how AI-assisted methods can help monitor, diagnose, and adapt simulation-based digital twins as operating conditions change. This is an emerging research direction, building on my earlier work in simulation, optimization, and multi-agent mobility systems.

<div class="research-area-clear"></div>

</section>

</div>
