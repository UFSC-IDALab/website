---
layout: page
permalink: /people/
title: people
description: academics and students from the lab
nav: true
nav_order: 4
display_categories: [academics, graduate, undergraduate]
horizontal: true
---

<div class="people">

{% if site.enable_project_categories and page.display_categories %}

  {% for category in page.display_categories %}
    <a id="{{ category }}" href=".#{{ category }}">
      <h2 class="category">{{ category | capitalize }}</h2>
    </a>

    {% assign categorized_people = site.people | where: "category", category %}
    {% assign sorted_people = categorized_people | sort: "importance" %}

    <div class="container">
      <div class="row">
        {% for person in sorted_people %}
          {% if category == "academics" %}
            <div class="col-12 col-md-6 mb-4">  <!-- 2 per row on md+ -->
              {% include people_horizontal.liquid person=person %}
            </div>
          {% else %}
            <div class="col-6 col-md-3 mb-4">  <!-- 4 per row on md+ -->
              {% include people.liquid person=person %}
            </div>
          {% endif %}
        {% endfor %}
      </div>
    </div>

  {% endfor %}

{% else %}

  {% assign sorted_people = site.people | sort: "importance" %}

  <div class="container">
    <div class="row">
      {% for person in sorted_people %}
        <div class="col-6 col-md-3 mb-4">  <!-- default 4 per row on md+ -->
          {% include people.liquid person=person %}
        </div>
      {% endfor %}
    </div>
  </div>

{% endif %}

</div>

<h2 class="category">Alumni</h2>
