---
title: Projects
icon: fas fa-user-secret
order: 5
---

## Projects Walkthroughs

Here are my latest Projects walkthroughs:

<ul>
{% for project in site.Projects %}
  <li>
    <a href="{{ site.baseurl }}{{ project.url }}">{{ project.title }}</a> - {{ project.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>