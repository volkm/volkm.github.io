---
layout: page
permalink: /tools/
title: Tools
description:
nav: true
nav_order: 3
display_categories: [model checking, fault tree, other]
horizontal: false
---

I develop and maintain several tools, especially for probabilistic model checking and fault tree analysis.
See my <a href="https://github.com/volkm">GitHub profile</a> for a complete list of my repositories and developer activities.

<!-- pages/tools.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized tools -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_tools = site.tools | where: "category", category %}
  {% assign sorted_tools = categorized_tools | sort: "importance" %}
  <!-- Generate cards for each tool -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_tools %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_tools %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display tools without categories -->

{% assign sorted_tools = site.tools | sort: "importance" %}

  <!-- Generate cards for each tool -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_tools %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_tools %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
