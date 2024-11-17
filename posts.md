---
layout: page
title: "Posts"
permalink: /posts
---
<h1> List of Posts </h1>
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
