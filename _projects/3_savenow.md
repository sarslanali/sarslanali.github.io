---
layout: page
title: SAVeNoW
permalink: /projects/savenow/
description: Funded research on lane-free traffic, human perception and the development of a dynamic driving-simulator test capability.
img: assets/img/projects/SAVeNoW/savenow-thumbnail.png
importance: 1
category: funded projects
---

<style>
  .savenow-page { --simulator-width: 51%; --framework-width: 53%; --pipeline-width: 45%; --matrix-width: 57%; }
  .savenow-page h2 { clear: both; }
  .savenow-figure { float: right; width: var(--figure-width); max-width: 100%; margin: 0.3rem 0 1rem 1.4rem; }
  .savenow-figure.left { float: left; margin: 0.3rem 1.4rem 1rem 0; }
  .savenow-figure img { display: block; width: 100%; height: auto; border-radius: 3px; }
  .savenow-figure figcaption { margin-top: 0.35rem; font-size: 0.75rem; line-height: 1.45; color: var(--global-text-color-light, #777); }
  @media (max-width: 720px) { .savenow-figure, .savenow-figure.left { float: none; width: 100%; margin: 1rem 0; } }
</style>

<div class="savenow-page" markdown="1">

**Funded research · 2021–2023 · Digital twins · Driving simulation · Human-centered automated mobility**

[**SAVeNoW project**](https://savenow.de/en/) · [**TUM project description**](https://www.mos.ed.tum.de/en/vt/forschung/projekte/abgeschlossene-projekte/savenow-compledet-2023/) · [**Simulator announcement**](https://www.mos.ed.tum.de/en/vt/news/article/new-cruden-driving-simulator/)

## Project overview

**SAVeNoW** (*Functional and Traffic Safety for Automated and Connected Mobility – Benefits for Society and Ecological Effects*) was an industry–academic research project led by Audi and supported by the German Federal Ministry of Transport. The project developed a **digital twin of Ingolstadt's urban traffic** for evaluating automated and connected mobility in terms of safety, traffic efficiency, environmental impacts and social acceptance.

At the Technical University of Munich (TUM), a key research direction was **lane-free traffic (LFT)**: exploring whether connected automated vehicles could use road space without conventional lane markings, and how humans would perceive such a traffic system. An important component was establishing a **dynamic driving-simulator capability** to investigate human responses in scenarios that would be difficult or unsafe to test on public roads.

## My contributions

<figure class="savenow-figure" style="--figure-width: var(--simulator-width);">
  <a href="{{ '/assets/img/projects/SAVeNoW/savenow-simulator.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/projects/SAVeNoW/savenow-simulator.jpg' | relative_url }}" alt="Dynamic six-degree-of-freedom Cruden driving simulator installed at TUM" loading="lazy"></a>
  <figcaption>Dynamic 6-DoF simulator installed at TUM.</figcaption>
</figure>

I contributed to TUM's SAVeNoW activities in two connected areas:

- **Research infrastructure:** Led the technical procurement process for a **Cruden AS2 dynamic driving simulator**, including defining technical requirements and specifications, collecting and comparing vendor offers, and developing evaluation and selection criteria. The simulator was installed at TUM in 2023 to support human-centered research on automated and lane-free driving.
- **Research methodology:** Co-authored a framework for investigating **perceived safety, comfort and human acceptance** of lane-free traffic using a dynamic driving simulator.
- **Experimental design:** Helped investigate requirements for simulator hardware, traffic-simulation integration and a structured set of test scenarios ranging from fully automated to mixed human–automated traffic.


## How can people experience lane-free traffic safely?

<figure class="savenow-figure left" style="--figure-width: var(--framework-width);">
  <a href="{{ '/assets/img/projects/SAVeNoW/savenow-framework.png' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/projects/SAVeNoW/savenow-framework.png' | relative_url }}" alt="Conceptual framework connecting lane-free traffic simulation, driving-simulator hardware and human responses" loading="lazy"></a>
  <figcaption>Proposed LFT driving-simulator framework.</figcaption>
</figure>

Conventional microscopic traffic simulations can assess capacity and vehicle trajectories, but they cannot directly reveal how a person **feels when surrounded by fast-moving vehicles without conventional lanes**. The research therefore examined the use of a motion-based simulator to study both **drivers and passengers** in realistic virtual traffic conditions.

Our 2023 paper proposed a conceptual architecture combining lane-free traffic scenarios with driving-simulation software, vehicle dynamics, displays, sound, motion feedback and human–machine interfaces. Particular emphasis was placed on representing **lateral movements, close vehicle spacing, and the transitions between automated and human-controlled driving**.

## Simulation integration and virtual environments

<figure class="savenow-figure" style="--figure-width: var(--pipeline-width);">
  <a href="{{ '/assets/img/projects/SAVeNoW/savenow-virtual-environment.jpg' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/projects/SAVeNoW/savenow-virtual-environment.jpg' | relative_url }}" alt="Proposed workflow linking road network and three-dimensional environment data with lane-free traffic simulation" loading="lazy"></a>
  <figcaption>Proposed virtual-environment development pipeline.</figcaption>
</figure>

A major technical challenge is connecting **microscopic traffic models** to immersive **3D driving environments**. Traditional road-network formats, such as OpenDRIVE, describe lane-based roads, so lane-free experiments require preprocessing and adjustments to both traffic movements and visual road geometry.

We proposed a modular workflow connecting road descriptions and virtual-environment generation with LFT control strategies and traffic simulation. For scenarios involving a **human-driven ego vehicle**, the paper highlights the need for bidirectional exchange: surrounding simulated vehicles must respond to the human driver's actions in real time.

## Research scenarios and human perception

<figure class="savenow-figure left" style="--figure-width: var(--matrix-width);">
  <a href="{{ '/assets/img/projects/SAVeNoW/savenow-scenario-matrix.png' | relative_url }}" target="_blank" rel="noopener noreferrer"><img src="{{ '/assets/img/projects/SAVeNoW/savenow-scenario-matrix.png' | relative_url }}" alt="Lane-free traffic scenario matrix varying vehicle automation, control strategies and road configurations" loading="lazy"></a>
  <figcaption>Scenario matrix for progressively more complex LFT experiments.</figcaption>
</figure>

We introduced a **scenario matrix** that organizes possible studies by levels of vehicle automation, human involvement and complexity of lane-free traffic control. It ranges from automated-vehicle passenger experiences to a human-driven ego vehicle interacting with reactive LFT, and eventually more complex mixed traffic.

The proposed research questions include whether **smaller lateral and longitudinal gaps** affect perceived safety, how **vehicle motion cues** influence comfort, and whether **human–machine interfaces** can improve understanding and trust. The paper discusses eye tracking, physiological sensing and surveys as possible methods of assessment, not as measurements already collected.

## Publications and project links

- **Sekeran, M., Syed, A. A., Lindner, J., Margreiter, M., & Bogenberger, K. (2023).** *Investigating Lane-Free Traffic with a Dynamic Driving Simulator.* IEEE ITSC. [DOI](https://doi.org/10.1109/ITSC57777.2023.10421947) — conceptual framework and scenario matrix; acknowledges SAVeNoW funding.
- **Sekeran, M., Rostami-Shahrbabaki, M., Syed, A. A., Margreiter, M., & Bogenberger, K. (2022).** *Lane-Free Traffic: History and State of the Art.* IEEE ITSC. [DOI](https://doi.org/10.1109/ITSC55140.2022.9922282) — supporting scientific background; the paper acknowledges a **separate DFG project**.
- [SAVeNoW official website](https://savenow.de/en/) · [TUM's SAVeNoW subproject](https://www.mos.ed.tum.de/en/vt/forschung/projekte/abgeschlossene-projekte/savenow-compledet-2023/) · [Cruden's simulator announcement](https://www.cruden.com/article/cruden-supplies-autonomous-driving-simulator-to-the-technical-university-of-munich) · [Mobility Innovation Campus](https://www.iabg.de/en/industries/automotive/mobility-innovation-campus)

<small>**Project context:** March 2021–June 2023; coordinator: Audi AG; total consortium budget: €10.75 million, including €7.71 million federal funding (German transport ministry). These are **consortium-wide figures**, not a budget personally managed by me.</small>

<small>**Figure credits:** The simulator photograph and Figs. 1, 3 and 4 are extracted from Sekeran et al. (2023), *IEEE ITSC*, DOI: 10.1109/ITSC57777.2023.10421947. © 2023 IEEE.</small>


</div>
