---
layout: page
permalink: /team/
title: Team
nav: true
nav_order: 1

team:
  - name: Hyeongrak Choi
    role: PI
    align: left
    image: Hyeongrak_Choi.jpeg
    content: about_Hyeongrak_Choi.md
    image_circular: false
    more_info: |
      <div>
        Office: Light Engineering 265<br>
        Email: hyeongrak.choi@stonybrook.edu<br>
        Phone: (617) 335-5420
      </div>

  - name: Jie Gu
    role: PhD
    align: left
    image: Jie_Gu.jpeg
    content: about_Jie_Gu.md
    image_circular: false
    more_info: |
      <div>
        Office: Light Engineering 150<br>
        Email: jie.gu@stonybrook.edu<br>
        Phone: (934) 451-9359
      </div>

  - name: Shaswata Mahernob Sarkar
    role: PhD
    align: left
    image: Shaswata_Mahernob_Sarkar.jpeg
    content: about_Shaswata_Mahernob_Sarkar.md
    image_circular: false
    more_info: |
      <div>
        Office: Light Engineering 150<br>
        Email: shaswatamahern.sarkar@stonybrook.edu<br>
        Phone: (934) 256-3787
      </div>
---

## Principal Investigator
{% assign pis = page.team | where: "role", "PI" %}
{% include profiles.html profiles=pis %}

## PhD Students
{% assign phd = page.team | where: "role", "PhD" %}
{% include profiles.html profiles=phd %}

## Master Students
{% assign ms = page.team | where: "role", "MS" %}
{% include profiles.html profiles=ms %}

## Undergraduate Interns
{% assign ug = page.team | where: "role", "UG" %}
{% include profiles.html profiles=ug %}

## Alumni
{% assign alumni = page.team | where: "role", "Alumni" %}
{% include profiles.html profiles=alumni %}
