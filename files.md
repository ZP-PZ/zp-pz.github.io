---
layout: default
title: Files
permalink: /files/
---

# Files

{% assign files = site.static_files | sort: "name" %}

<ul class="file-list">
{% for file in files %}
  {% if file.path contains '/assets/pdfs/' %}
    <li>
      <a href="{{ file.path | relative_url }}">
        {{ file.name }}
      </a>
    </li>
  {% endif %}
{% endfor %}
</ul>