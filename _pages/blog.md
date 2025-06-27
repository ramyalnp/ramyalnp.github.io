---
layout: default
title: Blog
description: Just my thoughts
permalink: /blog/
nav: true
nav_order: 2
---

<h1>{{ site.blog_name }}</h1>
<p>{{ site.blog_description }}</p>

<hr>

<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
      <p><strong>{{ post.date | date: "%B %d, %Y" }}</strong></p>
      <p>{{ post.description }}</p>
      <p><a href="{{ post.url | relative_url }}">Read more →</a></p>
      <hr>
    </li>
  {% endfor %}
</ul>