---
layout: default
title: People
nav_order: 2
---

# People

Click on an individual's name to learn more about them. Fill out [this form](https://forms.gle/WoNpfg4wn5sTCYZY9) if you want to be listed here.

<table>
    {% for person in site.data.people %}
    <tr>
      <td><a href="{{ person.name | datapage_url: 'people' }}">{{person.name}}</a></td>
      <td><b>{{ person.role }}, {{ person.department }}</b><br>{{ person.institution }}</td>
    </tr>
    {% endfor %}
</table>
