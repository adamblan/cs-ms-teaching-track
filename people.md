---
layout: default
title: People
nav_order: 2
---

# People

Click on an individual's name to learn more about them. Fill out [this form](https://forms.gle/WoNpfg4wn5sTCYZY9) if you want to be listed here.

{% for person in site.people %}
{{ person }}
{% endfor %}
