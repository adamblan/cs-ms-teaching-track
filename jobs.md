---
layout: default
title: Jobs
nav_order: 4
---

Content coming soon.

<table>
    {% for person in site.data.people %}
    <tr>
      <td><a href="{{ person.name | datapage_url: 'dogs' }}">{{person.name}}</a></td>
      <td><b>{{ person.role }}, {{ person.department }}</b><br>{{ person.institution }}</td>
    </tr>
    {% endfor %}
</table>
