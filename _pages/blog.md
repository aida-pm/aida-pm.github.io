---
layout: single
title: "Blog"
permalink: /blog/
author_profile: true
---

{% assign posts = site.posts | sort: 'date' | reverse %}
{% for post in posts limit:3 %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <p><em>{{ post.date | date: "%B %d, %Y" }}</em></p>
  <p>{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
  <a href="{{ post.url }}">Read more →</a>
  <hr>
{% endfor %}
