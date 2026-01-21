---
layout: page
permalink: /repositories/
title: Repositories
description: Repositories for our research.
nav: true
nav_order: 3
---

## QEP Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

## Contributed Repositories
