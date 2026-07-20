---
layout: default
title: Files
permalink: /files/
---

# Files

Documents stored in `assets/pdfs/`.

{% assign files = site.static_files | sort: "name" %}
{% for file in files %}
{% if file.path contains "/assets/pdfs/" %}
- [{{ file.name }}]({{ file.path | relative_url }})
{% endif %}
{% endfor %}