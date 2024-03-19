---
layout: archives
icon: fas fa-archive
order: 3
---
{% comment %}Combine posts and projects into a single array and sort them by date{% endcomment %}
{% assign combined_items = site.posts | concat: site.projects %}
{% assign sorted_items = combined_items | sort: 'date' %}

{% comment %}Group items by year and then by month{% endcomment %}
{% assign items_by_year = sorted_items | group_by_exp:"item", "item.date | date: '%Y'" %}
{% for year in items_by_year %}
  <h2>{{ year.name }}</h2>
  {% assign items_by_month = year.items | group_by_exp:"item", "item.date | date: '%B'" %}
  {% for month in items_by_month %}
    <h3>{{ month.name }}</h3>
    <ul>
      {% for item in month.items %}
        <li>
          <a href="{{ item.url }}">{{ item.title }}</a> - {{ item.date | date: "%b %d, %Y" }}
          {% if item.categories contains 'TryHackMe' %}
            <span>(TryHackMe Walkthrough)</span>
          {% elsif item.categories %}
            <span>({{ item.categories | join: ', ' }})</span>
          {% endif %}
        </li>
      {% endfor %}
    </ul>
  {% endfor %}
{% endfor %}