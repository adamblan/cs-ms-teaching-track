---
layout: default
title: Institutions
nav_order: 3
---

# Institutions

<table>
<tr>
  <td><b>Institution</b></td>
  <td><b>Titles</b></td>
</tr>
{% for row in site.data.institutions %}
<tr>
  <td>{{ row.institution }}</td>
  <td>{{ row.titles }}</td>
</tr>
{% endfor %}
