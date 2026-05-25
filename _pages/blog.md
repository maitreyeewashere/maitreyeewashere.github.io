---
layout: page
title: Blog
permalink: /blog
---

<div class="posts-grid">
{% for note in site.notes reversed %}
  <a class="post-card internal-link" href="{{ note.url }}">
    <div class="post-meta">{{ note.date | date: "%B %Y" }}</div>
    <h3>{{ note.title }}</h3>
    <p>{{ note.description }}</p>
  </a>
{% endfor %}
</div>

<style>
.posts-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 1.5em;
  margin-top: 2em;
}
.post-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 1.2em;
  display: block;
  border-bottom: 1px solid #e0e0e0;
  transition: box-shadow 200ms;
}
.post-card:hover {
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  background: #fffaf1;
}
.post-card h3 {
  margin: 0.3em 0;
  font-size: 1em;
}
.post-meta {
  font-size: 0.75em;
  color: #888;
}
.post-card p {
  font-size: 0.85em;
  color: #555;
  margin: 0.5em 0 0;
}
</style>
