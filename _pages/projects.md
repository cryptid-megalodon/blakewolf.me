---
title: Projects
permalink: /projects/
layout: page
---

# My Projects

{% if site.data.github_projects %}
<ul>
{% for project in site.data.github_projects.projects %}
  <li><strong><a href="{{ project.url }}">{{ project.name }}</a></strong> - {{ project.description }}{% if project.language %} <em>({{ project.language }})</em>{% endif %}</li>
{% endfor %}
</ul>

---

*Last updated: {{ site.data.github_projects.last_updated | date: "%B %d, %Y at %I:%M %p UTC" }}*
{% else %}
*Projects list is being generated. Please check back soon.*
{% endif %}