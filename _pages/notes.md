---
layout: page
title: Notes
permalink: /notes/
---

<h2>Course Notes</h2>

{% assign courses = site.notes | group_by_exp: "note", "note.path | split: '/' | slice: -2,1" %}

{% for course in courses %}
  <h3>{{ course.name }}</h3>
  <ul>
    {% for note in course.items %}
      <li><a href="{{ note.url }}">{{ note.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
