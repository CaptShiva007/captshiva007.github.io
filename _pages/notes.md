---
layout: default
title: Notes
permalink: /notes/
---

# Course Notes

{% for note in site.notes %}
- [{{ note.title }}]({{ note.url }})
{% endfor %}