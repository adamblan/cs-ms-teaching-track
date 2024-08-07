---
layout: default
title: Why Teaching?
nav_order: 2
parent: Quotes
---

# Why Teaching?
These are some of the responses we got when we asked: "How did you first decide you were interested in teaching?"

{% for person in site.people %}
{% if person.developed-interest %}
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
    <p>{{ person.developed-interest }}</p>
  </div>
</div>
{% endif %}
{% endfor %}
