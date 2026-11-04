---
layout: page
title: Projects
permalink: /projects/
description:
nav: true
nav_order: 2
display_categories: [software,funded projects]
horizontal: true
---

<style>
  .projects h2.category {
    text-align: left !important;
    color: var(--global-text-color) !important;
    font-size: 1.5rem !important;
    font-weight: 500;
    text-transform: capitalize;
    border-left: 4px solid var(--global-theme-color);
    padding-left: 12px;
    margin: 35px 0 20px;
    line-height: 1.3;
  }
  .projects > a { text-decoration: none !important; }

.projects .card .row.no-gutters { display: flex; flex-wrap: nowrap; align-items: center; }
.projects .card .row.no-gutters > div:first-child:not(:last-child) { flex: 0 0 180px; max-width: 180px; }
.projects .card .row.no-gutters > div:nth-child(2) { flex: 1; min-width: 0; }
.projects .card-img { width: 100%; height: 150px; object-fit: contain; }
.projects .card-body { padding: 12px; }

</style>

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display projects without categories -->

{% assign sorted_projects = site.projects | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
