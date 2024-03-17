---
title: Walkthroughs
icon: fas fa-user-secret
order: 5
---

## TryHackMe Walkthroughs

Here are my latest TryHackMe walkthroughs:

<ul>
{% for walkthrough in site.walkthroughs %}
  <li>
    <a href="{{ site.baseurl }}{{ walkthrough.url }}">{{ walkthrough.title }}</a> - {{ walkthrough.date | date: "%B %d, %Y" }}
  </li>
{% endfor %}
</ul>