---
layout: page
permalink: /repositories/
title: Github Repositories
description: Repositories for Programming Assignments
nav: true
nav_order: 4
---

<H3>Goals:</H3>

{% if site.data.repositories.github_repos %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
