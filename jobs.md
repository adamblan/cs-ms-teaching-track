---
layout: default
title: Jobs
nav_order: 4
---

# Job Postings

List of jobs posted for the current hiring cycle (2024-2025 hiring cycle) that do not require a PhD!

{% assign jobs = site.data.jobs-24-25 %}

{% for job in jobs %}

<div class="institution">
  <div>
    <h3 class="institution-name">
      {{job.institution}}
      {% if job.department %}
      <br>
      {{ job.department }}
      {% endif %}
    </h3>
    {% if job.title %}
    Hiring for the position of: {{ job.title }}
    <br>
    {% endif %}
    {% if job.link %}
    Full job posting: <a href="{{ job.link }}"> {{ job.link }} </a>
    <br>
    {% endif %}
    {% if job.posted %}
    Job posted on: {{ job.posted }}
    <br>
    {% endif %}
  </div>
</div>

---


{% endfor %}
