---
title: Blogs
icon: fas fa-user-secret
order: 5
---

## Blogs 

Here are my latest Blogs:

<ul>
{% for blog in site.blogs %}
  <li>
    <a href="{{ site.baseurl }}{{ blog.url }}">{{ blog.title }}</a> - {{ blog.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>