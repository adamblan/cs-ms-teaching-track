---
layout: default
title: Academic Paths
nav_order: 2
parent: Quotes
---

# Academic Paths
What was the path to your current position?

{% for person in site.people %}
{% if person.academic-path %}
<div class="staffer">
  {% if person.photo %}
  <img class="staffer-image" src="{{ person.photo }}" alt="">
  {% endif %}
  <div>
    <h3 class="staffer-name">
      {% if person.website %}
      <a href="{{ person.website }}">{{person.title}}</a>
      {% else %}
      {{person.title}}
      {% endif %}
      {% if person.pronouns %}
      <span class="staffer-pronouns">{{ person.pronouns }}</span>
      {% endif %}
    </h3>
    <p><b>{{ person.role }}, {{ person.department }}</b></p>
    <p>{{ person.institution }}</p>
    <p>{{ person.academic-path }}</p>
  </div>
</div>
{% endif %}
{% endfor %}
