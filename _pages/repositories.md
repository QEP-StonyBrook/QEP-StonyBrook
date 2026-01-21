---
layout: page
permalink: /repositories/
title: Repositories
description: Repositories for our research.
nav: true
nav_order: 3
---

## QEP Repositories

{% if site.data.repositories.github_repos and site.data.repositories.github_repos.size > 0 %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% else %}
_No QEP repositories configured in `_data/repositories.yml`._
{% endif %}

## Contributed Repositories

{% if site.data.repositories.github_repos_contributed and site.data.repositories.github_repos_contributed.size > 0 %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos_contributed %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% else %}
_No contributed repositories configured in `_data/repositories.yml`._
{% endif %}
