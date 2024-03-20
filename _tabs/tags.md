---
layout: tags
icon: fas fa-tags
order: 6
---

{% assign tag_list = site.tags | sort %}
{% for tag in tag_list %}
  <h2 id="{{ tag[0] }}">{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}