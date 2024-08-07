---
layout: default
title: Advice
nav_order: 1
parent: Quotes
---

# Advice
These are some of the responses we got when we asked: "What is one recommendation you have for someone just starting to consider teaching without a Ph.D.?"

{% for person in site.people %}
{% if person.recommendation %}
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
    <p>{{ person.recommendation }}</p>
  </div>
</div>
{% endif %}
{% endfor %}
