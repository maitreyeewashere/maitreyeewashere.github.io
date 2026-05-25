---
layout: page
title: Blog
permalink: /blog
---

{% for note in site.notes %}
  <div>
    <a href="{{ note.url }}">{{ note.title }}</a>
    <time>{{ note.date | date: "%B %d, %Y" }}</time>
  </div>
{% endfor %}
