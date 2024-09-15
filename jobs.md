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
    </h3>
    {% if job.department %}
      <b>Department of</b>: <i>{{ job.department }} </i>
      <br>
    {% endif %}
    {% if job.title %}
    <b>Hiring for the position of</b>: {{ job.title }}
    <br>
    {% endif %}
    {% if job.link %}
    <b>Full job posting</b>: <a href="{{ job.link }}"> {{ job.link }} </a>
    <br>
    {% endif %}
    {% if job.posted %}
    <b>Job posted on</b>: {{ job.posted }}
    <br>
    {% endif %}
    {% if job.notes %}
    <b>Other Notes</b>: {{ job.notes }}
    <br>
    {% endif %}
  </div>
</div>

---


{% endfor %}
