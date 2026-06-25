---
layout: default
title: Projects
permalink: /projects/
---

## Projects

These projects highlight my work across software engineering, graph-based data modeling, REST API integrations, and AI knowledge representation.

<div class="project-grid">
{% assign projects = site.projects | sort: "date" | reverse %}
{% for project in projects %}
  <div class="project-card">
    <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
    {% if project.tech %}<p class="project-tech">{{ project.tech | join: " &middot; " }}</p>{% endif %}
    <p>{{ project.content | strip_html | truncatewords: 34 }}</p>
    <div class="project-links">
      <a href="{{ project.url | relative_url }}">Read More &rarr;</a>
      {% if project.repo %}<a href="{{ project.repo }}" target="_blank" rel="noopener">Code &rarr;</a>{% endif %}
      {% if project.demo %}<a href="{{ project.demo }}" target="_blank" rel="noopener">Demo &rarr;</a>{% endif %}
    </div>
  </div>
{% endfor %}
</div>
