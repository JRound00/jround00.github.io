---
layout: archives
icon: fas fa-archive
order: 7
---
# Archives

## Blogs
{% assign blogs_by_year = site.blogs | sort: 'date' | reverse %}
{% for blog in blogs_by_year %}
  {% unless blog.previous %}
    <h2>{{ blog.date | date: '%Y' }}</h2>
  {% else %}
    {% unless blog.date | date: '%Y' == blog.previous.date | date: '%Y' %}
      <h2>{{ blog.date | date: '%Y' }}</h2>
    {% endunless %}
  {% endunless %}
  <h3>{{ blog.date | date: '%B' }}</h3>
  <ul>
    {% for blog in blogs_by_year %}
      {% if blog.date | date: '%Y' == blog.previous.date | date: '%Y' and blog.date | date: '%B' == blog.previous.date | date: '%B' %}
        <li><a href="{{ blog.url | prepend: site.baseurl }}">{{ blog.title }}</a> - {{ blog.date | date: "%B %d, %Y" }}</li>
      {% endif %}
    {% endfor %}
  </ul>
{% endfor %}

## Projects
<!-- Repeat the same structure for projects -->
{% assign projects_by_year = site.projects | sort: 'date' | reverse %}
<!-- Insert the Liquid templating logic similar to the Blogs section -->

## Walkthroughs
<!-- Repeat the same structure for walkthroughs -->
{% assign walkthroughs_by_year = site.walkthroughs | sort: 'date' | reverse %}
<!-- Insert the Liquid templating logic similar to the Blogs section -->