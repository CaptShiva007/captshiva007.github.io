---
layout: default
title: Notes
permalink: /notes/
---

# Course Notes

{% assign notes = site.static_files | where: "path", "/notes/AZ900" %}
{% for note in notes %}
- [{{ note.name }}]({{ note.path }})
{% endfor %}