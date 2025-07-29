---
title: Projects
permalink: /projects/
layout: page
---

# My Projects

Below is an automatically updated list of my GitHub projects that have descriptions. Each project links to its GitHub repository where you can find detailed README files and source code.

{% if site.data.github_projects %}
{% for project in site.data.github_projects.projects %}
* **[{{ project.name }}]({{ project.url }})** - {{ project.description }}{% if project.language %} *({{ project.language }})*{% endif %}
{% endfor %}

---

*Last updated: {{ site.data.github_projects.last_updated | date: "%B %d, %Y at %I:%M %p UTC" }}*
{% else %}
*Projects list is being generated. Please check back soon.*
{% endif %}