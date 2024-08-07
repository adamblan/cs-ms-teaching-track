---
layout: default
title: Data
nav_order: 4
---

# Data about Jobs
We've asked current faculty who are teaching without a Ph.D. at various institutions, in various stages of their careers, to answer some questions about their current positions.  

{% assign peeps = site.people | sort: 'institution' %}

## How many years is your contract?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>Contract Length</b></td>
</tr>

{% for person in peeps %}
{% if person.contract-length %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.contract-length }}</td>
</tr>
{% endif %}
{% endfor %}
</table>

## How many courses do you teach in a term (quarter/semester)?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>Term Load</b></td>
</tr>

{% for person in peeps %}
{% if person.term-load %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.term-load }} ({{person.term-type}})</td>
</tr>
{% endif %}
{% endfor %}
</table>

## What kinds of courses do you teach?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>Courses</b></td>
</tr>

{% for person in peeps %}
{% if person.courses %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.courses }}</td>
</tr>
{% endif %}
{% endfor %}
</table>

## What kinds of service (if any) do you do at the department level?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>Department Service</b></td>
</tr>

{% assign no-dept-service = 0 %}
{% for person in peeps %}
{% if person.department-service %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.department-service }}</td>
</tr>
{% else %}
{% assign no-dept-service = no-dept-service | plus: 1 %}
{% endif %}
{% endfor %}
</table>
<em>{{no-dept-service}} other people left this answer empty, probably meaning that they do not do department level service.</em>

## What kinds of service (if any) do you do at the college or institution level?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>College Service</b></td>
</tr>

{% assign no-college-service = 0 %}
{% for person in peeps %}
{% if person.college-service %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.college-service }}</td>
</tr>
{% else %}
{% assign no-college-service = no-college-service | plus: 1 %}
{% endif %}
{% endfor %}
</table>
<em>{{no-college-service}} other people left this answer empty, probably meaning that they do not do college or institution level service.</em>

## What kinds of research (if any) do you do?
<table>
<tr>
  <td><b>Person</b></td>
  <td><b>Institution</b></td>
  <td><b>Research</b></td>
</tr>
{% assign no-research = 0 %}
{% for person in peeps %}
{% if person.college-service %}
<tr>
  <td>{{ person.name }} </td>
  <td>{{ person.institution }}</td>
  <td>{{ person.research }}</td>
</tr>
{% else %}
{% assign no-research = no-research | plus: 1 %}
{% endif %}
{% endfor %}
</table>
<em>{{no-research}} other people left this answer empty, probably meaning that they do not do research.</em>

