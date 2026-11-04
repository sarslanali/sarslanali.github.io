---
layout: about
title: About
permalink: /
subtitle: Researcher in Transportation Systems, Optimization, Simulation & AI

profile:
  align: right
  image: prof_pic_2.jpeg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>arslanali.syed@outlook.com</p>
    <p>Location: Munich, Germany</p>
    <p>Picture taken in Switzerland, and the credit goes to my wife</p>
    <p style="display:flex; gap:16px; font-size:1.7rem;">
      <a href="/assets/pdf/CV.pdf" title="Download CV" target="_blank"> <i class="ai ai-cv"></i> </a>
      <a href="mailto:arslanali.syed@outlook.com" title="Email"><i class="fa-solid fa-envelope"></i></a>
      <a href="https://scholar.google.com/citations?user=hUpg_fQAAAAJ" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
      <a href="https://www.linkedin.com/in/arslan-ali-syed" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>
      <a href="https://orcid.org/0000-0003-4929-1307" title="ORCID"><i class="ai ai-orcid"></i></a>
      <a href="https://www.researchgate.net/profile/Arslan-Ali-13" title="ResearchGate" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-researchgate"></i></a>
      <a href="https://github.com/sarslanali" title="GitHub"><i class="fa-brands fa-github"></i></a>
    </p>

selected_papers: true
scholar:
  sort_by: selected_order
  order: ascending

social: false # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

## About Me

I am a researcher and engineer specializing in transportation systems, optimization, simulation, and machine learning. 
I hold a Ph.D. from the Technical University of Munich (TUM) and have nearly a decade of academic and industrial 
research and development experience at TUM, BMW Group, and Infineon Technologies.

At TUM, I led the research group **Test Fields and Simulators**. I was a founding co-developer of FleetPy, an agent-based 
simulation framework for mobility services that has been used in multiple research projects and publications at TUM. 
I subsequently expanded my research into connected autonomous vehicles and developed LaneFreeDrive, a modular library 
for lane-free traffic simulation and control algorithms.


<style>
.featured { margin: 50px 0 35px; }
.featured h2 { font-size: 1.5rem; margin-bottom: 20px; }
.featured-item { display: flex; align-items: center; gap: 20px; margin-bottom: 22px; }
.featured-item img { width: 120px; max-width: 30vw; height: auto; }
.featured-item p { font-size: 0.88rem; margin: 5px 0; }
.profile .more-info a { color: var(--global-text-color) !important; }
.profile .more-info a:hover { color: var(--global-theme-color) !important; }
</style>

<div class="featured">
<h2>Featured Software</h2>

<div class="featured-item">
  <a href="{{ '/software/fleetpy/' | relative_url }}">
    <img src="{{ '/assets/img/projects/FleetPy/fleetpy.png' | relative_url }}" alt="FleetPy">
  </a>
  <div><b>FleetPy</b>
    <p>Open-source simulation framework for mobility-on-demand services and fleet optimization.</p>
    <a href="{{ '/software/fleetpy/' | relative_url }}">Learn more →</a>
  </div>
</div>

<div class="featured-item">
  <a href="{{ '/software/lanefreedrive/' | relative_url }}">
    <img src="{{ '/assets/img/projects/LaneFreeDrive/lanefreedrive-thumbnail.png' | relative_url }}" alt="LaneFreeDrive">
  </a>
  <div><b>LaneFreeDrive</b>
    <p>Modular simulation framework for lane-free traffic and connected autonomous vehicles.</p>
    <a href="{{ '/software/lanefreedrive/' | relative_url }}">Learn more →</a>
  </div>
</div>
</div>



<style>
  .cv-summary {
    --heading-size: 1.5rem;      /* Section headings */
    --title-size: 0.95rem;       /* Institution names */
    --role-size: 0.88rem;        /* Position / degree */
    --date-size: 0.80rem;        /* Dates */
    --text-size: 0.88rem;        /* Description */
    --line-height: 1.5;         /* Text line spacing */
    --entry-gap: 22px;          /* Space between entries */
    --description-gap: 6px;     /* Space above descriptions */
    --logo-size: 60px;          /* Logo dimensions */
  }

  .cv-summary h2 { font-size: var(--heading-size); margin: 30px 0 20px; }
  .cv-entry { display: flex; align-items: center; gap: 20px; margin-bottom: var(--entry-gap); }
  .cv-entry img { width: var(--logo-size); height: var(--logo-size); object-fit: contain; flex-shrink: 0; }
  .cv-entry .details { flex: 1; min-width: 0; line-height: var(--line-height); }
  .cv-entry .institution { font-size: var(--title-size); font-weight: 450; }
  .cv-entry .role { font-size: var(--role-size); font-weight: 400; }
  .cv-entry .date { font-size: var(--date-size); color: var(--global-text-color-light, #777); }
  .cv-entry .description { font-size: var(--text-size); margin-top: var(--description-gap); }
</style>

<div class="cv-summary">

<h2>Professional Experience</h2>

<div class="cv-entry">
  <img src="{{ '/assets/img/tum.png' | relative_url }}" alt="TUM logo">
  <div class="details">
    <div class="institution">Technical University of Munich (2021–2025)</div>
    <div class="role">Postdoctoral Researcher and Group Leader <span class="date">(Feb 2024 – Oct 2025)</span></div>
    <div class="role">Research Associate <span class="date">(Feb 2021 – Feb 2024)</span></div>
    <div class="description">Research in optimization, simulation, autonomous vehicles, and mobility digital twins.</div>
  </div>
</div>

<div class="cv-entry">
  <img src="{{ '/assets/img/bmw.png' | relative_url }}" alt="BMW logo">
  <div class="details">
    <div class="institution">BMW Group (2017–2020)</div>
    <div class="role">Research Associate – Mobility Services</div>
    <div class="description">
        Developed fleet management algorithms using mathematical optimization and machine learning.
        <p>Named inventor on six published European patent applications</p>.
        <a href="{{ '/patents/' | relative_url }}">View patent applications →</a>
    </div>
  </div>
</div>

<div class="cv-entry">
  <img src="{{ '/assets/img/infineon.png' | relative_url }}" alt="Infineon logo">
  <div class="details">
    <div class="institution">Infineon Technologies (2015–2017)</div>
    <div class="role">Analog Circuit Simulator Developer</div>
    <div class="description">Developed numerical methods for high-performance circuit simulation.</div>
  </div>
</div>

<h2>Education</h2>

<div class="cv-entry">
  <img src="{{ '/assets/img/tum.png' | relative_url }}" alt="TUM logo">
  <div class="details">
    <div class="institution">Technical University of Munich (2024)</div>
    <div class="role">Ph.D. (Dr.-Ing.) Transportation Engineering</div>
    <div class="description">Optimization of Autonomous Mobility-on-Demand Services.</div>
  </div>
</div>

<div class="cv-entry">
  <img src="{{ '/assets/img/tum.png' | relative_url }}" alt="TUM logo">
  <div class="details">
    <div class="institution">Technical University of Munich (2016)</div>
    <div class="role">M.Sc. Computational Science and Engineering </div>
  </div>
</div>

<div class="cv-entry">
  <img src="{{ '/assets/img/nust.jpg' | relative_url }}" alt="NUST logo">
  <div class="details">
    <div class="institution">National University of Sciences and Technology (2012)</div>
    <div class="role">B.E. Avionics Engineering</div>
  </div>
</div>

<a href="{{ '/cv/' | relative_url }}">View detailed CV →</a>

</div>
