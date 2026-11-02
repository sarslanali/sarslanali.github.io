---
layout: page
title: FleetPy
description: Open-source, modular agent-based simulation for mobility-on-demand services and fleet optimization.
img: assets/img/projects/FleetPy/fleetpy.png
importance: 1
category: software
permalink: /software/fleetpy/
---

<style>
  .fleetpy-page { --architecture-width: 43%; --control-width: 40%; --benchmarks-width: 48%; }
  .fleetpy-page h2 { clear: both; }
  .fleetpy-figure { float: right; width: var(--figure-width); max-width: 100%; margin: 0.35rem 0 1rem 1.5rem; }
  .fleetpy-figure.left { float: left; margin: 0.35rem 1.5rem 1rem 0; }
  .fleetpy-figure img { display: block; width: 100%; height: auto; }
  .fleetpy-figure figcaption { margin-top: 0.4rem; font-size: 0.75rem; line-height: 1.45; color: var(--global-text-color-light, #666); }
  .fleetpy-figure a:focus-visible { outline: 2px solid currentColor; }
  @media (max-width: 720px) {
    .fleetpy-figure, .fleetpy-figure.left { float: none; width: 100%; margin: 1rem 0; }
  }
</style>

<div class="fleetpy-page" markdown="1">

**Open-source research software · Mobility-on-demand · Fleet management · Python**

[**Source code**](https://github.com/TUM-VT/FleetPy) · [**Peer-reviewed paper (2026)**](https://doi.org/10.1186/s12544-026-00823-3) · [**Reproducible study**](https://github.com/TUM-VT/FleetPy/tree/main/studies/paper_2025_applications)

## Overview

FleetPy is an open-source, agent-based simulation framework developed at the Technical University of Munich for **mobility-on-demand (MoD) services**. It enables researchers to evaluate ride-hailing, ride-pooling, fleet operations and different service designs within a consistent simulation environment. Its modular architecture supports comparisons of algorithms and scenarios without rebuilding the entire simulation for each research question.

## Framework architecture

<figure class="fleetpy-figure" style="--figure-width: var(--architecture-width);">
  <a href="{{ '/assets/img/projects/FleetPy/fleetpy-architecture.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size FleetPy architecture showing its principal modules and interactions">
    <img src="{{ '/assets/img/projects/FleetPy/fleetpy-architecture.webp' | relative_url }}" alt="FleetPy architecture showing its principal modules and interactions" loading="lazy">
  </a>
  <figcaption>Figure 2. Main FleetPy modules and interactions. <a href="https://doi.org/10.1186/s12544-026-00823-3">Source</a> (<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>).</figcaption>
</figure>

FleetPy separates the main components of an MoD system: **customer demand and behavior**, **street networks and routing**, **mobility operators**, **fleet control**, **public transport**, and the interaction between users and providers through a **mobility broker**. The modules can be configured or extended independently.

This makes it possible to change fleet-control strategies while retaining the same scenario, demand inputs, and routing assumptions. It also lets researchers extend a specific module without replacing the rest of the simulation framework.

## Fleet optimization and simulation capabilities

<figure class="fleetpy-figure left" style="--figure-width: var(--control-width);">
  <a href="{{ '/assets/img/projects/FleetPy/fleetpy-control.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size Overview of the FleetPy fleet-control module and its submodules">
    <img src="{{ '/assets/img/projects/FleetPy/fleetpy-control.webp' | relative_url }}" alt="Overview of the FleetPy fleet-control module and its submodules" loading="lazy">
  </a>
  <figcaption>Figure 4. Fleet-control module. <a href="https://doi.org/10.1186/s12544-026-00823-3">Source</a> (<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>).</figcaption>
</figure>

The framework includes interchangeable fleet-control methods for **vehicle–request assignment, vehicle repositioning, trip offers and pricing, and charging**. It supports immediate-request and batch-offer simulation flows, allowing different operational policies to be evaluated under shared assumptions. Outputs include service rates, waiting and travel times, vehicle occupancy, empty kilometers, operating costs, and other performance indicators.

The modular fleet-control architecture separates operator-level decisions from the underlying simulation. Researchers can compare alternative strategies under common demand and network conditions, helping make the performance differences more interpretable.

## My contributions

I was a **founding co-developer of FleetPy** at TUM. My work included:

- Contributing to the framework's conceptualization, methodology, and software development.
- Developing and improving **demand forecasting, vehicle repositioning, and request-assignment methods** for mobility-on-demand services.
- Supporting reusable simulation and optimization workflows used across research projects.

The framework has been used in **several TUM research projects**. FleetPy is a collaborative project; the paper credits a broader team of contributors.

## Reproducibility and case studies

<figure class="fleetpy-figure" style="--figure-width: var(--benchmarks-width);">
  <a href="{{ '/assets/img/projects/FleetPy/fleetpy-benchmarks.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Open full-size FleetPy benchmark networks and demand distributions in Chicago, Manhattan and Munich">
    <img src="{{ '/assets/img/projects/FleetPy/fleetpy-benchmarks.webp' | relative_url }}" alt="FleetPy benchmark networks and demand distributions in Chicago, Manhattan and Munich" loading="lazy">
  </a>
  <figcaption>Figure 6. Benchmark networks, access nodes and demand distributions for Chicago, Manhattan and Munich. <a href="https://doi.org/10.1186/s12544-026-00823-3">Source</a> (<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>).</figcaption>
</figure>

The project provides standardized benchmark datasets for **Manhattan, Chicago, and Munich**, allowing researchers to test operational strategies in different urban contexts. The 2026 paper illustrates this with an assignment-algorithm comparison and a multi-operator scenario examining trade-offs between ride-hailing and ride-pooling.

The benchmarks support evaluation of simulation and fleet-control strategies across different urban contexts. Linked example configurations and analysis workflows allow others to reproduce and adapt the published experiments.

## Links and references

- **Code:** [github.com/TUM-VT/FleetPy](https://github.com/TUM-VT/FleetPy)
- **Paper:** Engelhardt, R., Dandl, F., Syed, A. A., et al. (2026). *FleetPy: an open source simulator for reproducible research on mobility-on-demand services.* European Transport Research Review, **18**, 52. [DOI: 10.1186/s12544-026-00823-3](https://doi.org/10.1186/s12544-026-00823-3)
- **Reproducible study:** [Example study, configurations and analysis notebook](https://github.com/TUM-VT/FleetPy/tree/main/studies/paper_2025_applications)

<small>**Image credits:** Figures 2, 4 and 6 reproduced unchanged from Engelhardt et al. (2026), published under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).</small>

</div>
