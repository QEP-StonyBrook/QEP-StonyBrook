---
layout: page
title: Devices
permalink: /devices/
nav: true
nav_order: 4
display_categories: 
horizontal: false
---
<!-- pages/devices.md -->
<div class="devices">
{% if site.enable_device_categories and page.display_categories %}
  <!-- Display categorized devices -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_devices = site.devices | where: "category", category %}
  {% assign sorted_devices = categorized_devices | sort: "importance" %}
  <!-- Generate cards for each device -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for device in sorted_devices %}
      {% include devices_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for device in sorted_devices %}
      {% include devices.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display devices without categories -->

{% assign sorted_devices = site.devices | sort: "importance" %}

  <!-- Generate cards for each device -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for device in sorted_devices %}
      {% include devices_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for device in sorted_devices %}
      {% include devices.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
