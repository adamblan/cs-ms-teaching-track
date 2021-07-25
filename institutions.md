---
layout: default
title: Institutions
nav_order: 3
---

# Institutions

The following list of institutions are known to hire teaching faculty who do not have Ph.D.'s.

<table>
<tr>
  <td><b>Institution</b></td>
  <td><b>Titles</b></td>
</tr>
{% assign insts = site.data.institutions | sort: 'institution' %}

{% for row in insts %}
<tr>
  <td>{{ row.institution }}</td>
  <td>{{ row.titles }}</td>
</tr>
{% endfor %}
