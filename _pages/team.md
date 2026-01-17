---
layout: profiles
permalink: /team/
title: Team
description: members of the lab or group
nav: true
nav_order: 1

profiles:
  {% for person in site.data.team %}
  - align: {{ person.align }}
    image: {{ person.image }}
    image_circular: {{ person.image_circular }}

    content: |
      {{ person.bio | markdownify }}

    more_info: |
      {% if person.office %}<p>{{ person.office }}</p>{% endif %}
      {% if person.email %}<p>{{ person.email }}</p>{% endif %}
      {% if person.phone %}<p>{{ person.phone }}</p>{% endif %}
      {% if person.address %}<p>{{ person.address }}</p>{% endif %}
      {% if person.city %}<p>{{ person.city }}</p>{% endif %}
  {% endfor %}
---
