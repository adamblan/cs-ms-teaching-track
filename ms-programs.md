---
layout: default
title: MS Programs
nav_order: 6
---

# MS Programs

The following is a list of institutions with MS programs that are known to help prepare students to be teaching faculty. There aren't a lot of these, and each of them handle things differently.

{% assign progs = site.data.ms-programs | sort: 'institution' %}

{% for prog in progs %}

<div class="institution">
  <div>
    <h3 class="institution-name">
      {{prog.institution}}
      {% if prog.location %}
      <span class="institution-location">{{ prog.location }}</span>
      {% endif %}
    </h3>
    <ul>
    {% for note in prog.notes %}
      <li> {{note}} </li>
    {% endfor %}
    </ul>
  </div>
</div>

---

{% endfor %}
