---
layout: default
title: People
nav_order: 2
---

# People

This is a collection of individuals who are all teaching faculty and do not have a PhD.
Click on an individual's name to learn more about them. Fill out [this form](https://forms.gle/WoNpfg4wn5sTCYZY9) if you want to be listed here.

{% for person in site.people %}
{{ person }}
{% endfor %}
