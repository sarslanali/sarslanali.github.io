---
layout: page
title: München elektrisiert (Mᵉ)
description: EV charging strategies and public charging infrastructure for electric ride-pooling, evaluated using FleetPy in Munich.
img: assets/img/projects/MuenchenElektrisiert/thumbnail.png
importance: 5
category: funded projects
permalink: /projects/muenchen-elektrisiert/
---

<style>
  .me-project { --search-width: 56%; --search-results-width: 46%; --mod-width: 40%; --mod-results-width: 46%; --figure-gap: 1.25rem; --caption-size: .76rem; }
  .me-project .me-figure { width: var(--figure-width); max-width: 100%; float: right; margin: .25rem 0 1rem var(--figure-gap); }
  .me-project .me-figure.left { float: left; margin: .25rem var(--figure-gap) 1rem 0; }
  .me-project .me-figure img { display: block; width: 100%; height: auto; border-radius: 4px; }
  .me-project .me-figure figcaption { font-size: var(--caption-size); line-height: 1.4; margin-top: .35rem; color: var(--global-text-color-light, #777); }
  .me-project .me-clear { clear: both; }
  @media (max-width: 640px) { .me-project .me-figure, .me-project .me-figure.left { float: none; width: 100%; margin: 1rem 0; } }
</style>

<div class="me-project" markdown="1">

## Project overview

**München elektrisiert (Mᵉ)** was a publicly funded research and infrastructure project (2018–2022) to support electric mobility in Munich through improved charging infrastructure and smarter charging strategies. At the **Technical University of Munich (TUM), Chair of Traffic Engineering and Control**, I contributed to **two research work packages**, using and extending the open-source **FleetPy** simulation framework to investigate how public charging infrastructure could be used more efficiently.

**My focus:** agent-based simulation, charging-point search and reservation policies, electric fleet operation, and assessment of charging infrastructure utilization.

## **1. Charging-point search and reservation strategies**

<figure class="me-figure" style="--figure-width: var(--search-width);">
  <a href="{{ '/assets/img/projects/MuenchenElektrisiert/charging-search-policies.png' | relative_url }}"><img src="{{ '/assets/img/projects/MuenchenElektrisiert/charging-search-policies.png' | relative_url }}" alt="Comparison of manual, informed and reservation-based EV charging-point search strategies" loading="lazy"></a>
  <figcaption>Manual, informed, and reservation-based charging-point search (Syed et al., IEEE ITSC 2022, Fig. 2).</figcaption>
</figure>

I investigated how drivers could reduce unnecessary detours when searching for public EV chargers. Using a modified version of FleetPy for private and commercial vehicle trips, we compared three strategies:

- **Direct search:** Drivers visit nearby charging stations to look for a free point.
- **Informed search:** Drivers use real-time charger availability information.
- **Reservation:** Drivers can reserve an available charging point before arrival.

The simulations used Munich's road network, public charging infrastructure, and synthetic daily EV trips. We measured additional driving distance, walking distance, charging-station utilization, and search success rates.

<div class="me-clear"></div>

<figure class="me-figure" style="--figure-width: var(--search-results-width);">
  <a href="{{ '/assets/img/projects/MuenchenElektrisiert/charging-search-results.png' | relative_url }}"><img src="{{ '/assets/img/projects/MuenchenElektrisiert/charging-search-results.png' | relative_url }}" alt="Simulation results for EV charging point search strategies" loading="lazy"></a>
  <figcaption>Charging-search performance across different search radii (Syed et al., IEEE ITSC 2022, Fig. 5).</figcaption>
</figure>

### Key simulation results:

With a 500 m search radius and 100% adoption, informed search reduced the *additional distance driven to find charging* by **54.4%**, and reservation-based search by **69.0%**, relative to direct search. At 50% adoption the respective reductions were **27.3%** and **30.4%**. These were model-based estimates under the study's assumptions, not observed reductions in citywide traffic.

### My contribution:
I was the main contributor of this research. I developed and evaluated FleetPy-based charging-point search scenarios and their operational implications.

<div class="me-clear"></div>

## **2. Public charging for electric ride-pooling fleets**

<figure class="me-figure" style="--figure-width: var(--mod-width);">
  <a href="{{ '/assets/img/projects/MuenchenElektrisiert/mod-charging-infrastructure.png' | relative_url }}"><img src="{{ '/assets/img/projects/MuenchenElektrisiert/mod-charging-infrastructure.png' | relative_url }}" alt="Map of MoD operating area and charging infrastructure used in FleetPy for Munich, Germany" loading="lazy"></a>
  <figcaption>Map of MoD operating area and charging infrastructure used in FleetPy for Munich, Germany (Zhang et al., IEEE ITSC 2022, Fig. 2).</figcaption>
</figure>

I also contributed to a collaborative study of **electric mobility-on-demand (MoD) and ride-pooling fleets** using public chargers shared with private vehicles. This work extended FleetPy's charging simulation to represent station availability, charger bookings, vehicle state of charge, and charging-related repositioning journeys.

The study compared three charging arrangements in Munich: a **single operator depot**, **multiple operator depots**, and **existing public charging stations**. Public-charger occupancy was informed by empirical private-vehicle charging records. FleetPy was used to assess passenger level of service, charging-related empty mileage, and public-infrastructure utilization.

<div class="me-clear"></div>

<figure class="me-figure" style="--figure-width: var(--mod-results-width);">
  <a href="{{ '/assets/img/projects/MuenchenElektrisiert/mod-comparison-results.png' | relative_url }}"><img src="{{ '/assets/img/projects/MuenchenElektrisiert/mod-comparison-results.png' | relative_url }}" alt="Comparison of passenger service level and charging mileage under depot and public charging scenarios" loading="lazy"></a>
  <figcaption>Passenger service level and charging-related mileage for different infrastructure scenarios (Zhang et al., IEEE ITSC 2022, Figs. 4–5).</figcaption>
</figure>

### Key simulation results:

Using public charging infrastructure maintained **similar passenger service levels** to depot-only scenarios while requiring **substantially less extra driving for charging** than a single central depot. The results suggest an opportunity to use public charging infrastructure without building numerous dedicated depots, subject to local charging demand and availability.

### My contribution:

I contributed as a **co-author and FleetPy developer** to this collaborative simulation study. 
I further refined the class structure I developed for charge point search research was further extended and incorporated into FleetPy for this study.

<div class="me-clear"></div>

## Publications and links

- **Syed, A. A.**, Fischer, M., Hardt, C., & Bogenberger, K. (2022). [Charge Point Search Policies for EVs — Minimizing the Cruise for Juice](https://doi.org/10.1109/ITSC55140.2022.9921802). *IEEE ITSC 2022*.
- Zhang, Y., Engelhardt, R., **Syed, A.-A.**, Dandl, F., Hardt, C., & Bogenberger, K. (2022). [Simulating Charging Processes of Mobility-On-Demand Services at Public Infrastructure: Can Operators Complement Each Other?](https://doi.org/10.1109/ITSC55140.2022.9922449). *IEEE ITSC 2022*.
- [Official TUM project description](https://www.mos.ed.tum.de/vt/forschung/projekte/abgeschlossene-projekte/muenchen-elektrisiert-abgeschlossen-2022/) · [FleetPy on GitHub](https://github.com/TUM-VT/FleetPy)

<small>**Funding:** German Federal Ministry for Economic Affairs and Energy (BMWi), project *München elektrisiert*, grant **01MZ18010C**. **Figure credits:** IEEE ITSC 2022 papers linked above; reuse of the reproduced figures on a public website may require permission from the rights holder.</small>

</div>
