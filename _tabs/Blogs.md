---
title: Walkthroughs
icon: fas fa-user-secret
order: 5
---

## Blog Walkthroughs

Here are my latest Blog walkthroughs:

<ul>
{% for blog in site.Blogs %}
  <li>
    <a href="{{ site.baseurl }}{{ blog.url }}">{{ blog.title }}</a> - {{ blog.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>