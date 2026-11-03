---
layout: about
title: About
permalink: /
#subtitle: <a href='#'>Affiliations</a>. Address. Contacts. Motto. Etc.
subtitle: Munich based researcher for Transportation, Mobility Systems & Logistics <br> Expertise in Scientific Computing, Simulation, Optimization and Machine Learning

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p>arslanali.syed@outlook.com</p>
    <p>Location: Munich, Germany</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
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

## Hi, welcome to my website!

I am a researcher and engineer with a Ph.D. in Transportation Engineering and an M.Sc. in Computational Science and 
Engineering from the Technical University of Munich (TUM), and nearly nine years of combined academic and industrial 
experience at TUM and BMW Group. In my last role at TUM, I also led the research group **Test Fields and Simulators**.

My research interests include transportation and mobility systems, logistics, fleet management, connected and autonomous
vehicles, and mobility digital twins. My work combines mathematical optimization, agent-based simulation, demand forecasting, 
artificial intelligence, and machine learning to develop efficient and sustainable solutions for complex systems.


<style>
.featured { margin: 50px 0 35px; }
.featured h2 { font-size: 1.5rem; margin-bottom: 20px; }
.featured-item { display: flex; align-items: center; gap: 20px; margin-bottom: 22px; }
.featured-item img { width: 120px; max-width: 30vw; height: auto; }
.featured-item p { font-size: 0.88rem; margin: 5px 0; }
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
    <div class="description">Developed fleet management algorithms using mathematical optimization and machine learning.</div>
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
