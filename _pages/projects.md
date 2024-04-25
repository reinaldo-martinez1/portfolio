---
layout: page
title: Projects
permalink: /projects/
description: Best course's assignment
nav: true
nav_order: 3
display_categories: [writing, programming]
horizontal: false
---

<H3>Goals as a student of Artificial Intelligence:</H3>

1. One of my objectives is to become proficient in AI technologies through this course. By deepening my understanding of AI algorithms, techniques, and applications, I will be able to enhance my competitiveness for roles that requires AI applications.

2. I intend to identify opportunities to leverage AI techniques to solve complex problems and optimize processes within my future role as a computer engineer.

3. As I deepend my knowledge in artificial intelligence, I aspire to contribute to AI research and innovation. Whether it's through publishing papers, being in conferences or sharing my progress in personal projects with people from the industry.

4. My ultimate goal is to achieve the course objectives to improve my position as a student of computer engineering and using the knowledge acquired to further advance and explore opportunities of internships/research in the field of AI.

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
