---
layout: page
title: Blog Archive
---

<div class="archive-container">
{% for tag in site.tags %}
  <div class="archive-tag">
    <h3>{{ tag[0] }}</h3>
    <ul class="archive-list">
      {% for post in tag[1] %}
        <li><a href="{{ post.url }}">{{ post.date | date: "%B %Y" }} - {{ post.title }}</a></li>
      {% endfor %}
    </ul>
  </div>
{% endfor %}
</div>