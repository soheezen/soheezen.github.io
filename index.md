---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: home
---

<div class="intro">

# Ee Zen

I am a mathematics undergraduate at the National University of Singapore.

My main interests are in algebra, particularly representation theory,
cluster algebras, algebraic geometry, and related areas.

<div class="home-links">
<a href="/resume.pdf">CV</a>
<a href="YOUR-GITHUB">GitHub</a>
<a href="mailto:YOUR-EMAIL">Email</a>
</div>

</div>

<div class="home-section">

## Mathematics

I am currently interested in cluster algebras and their connections with
representation theory and algebraic geometry.

Some things I have been reading about include Richardson varieties,
Kac–Moody groups, and braid varieties.

</div>

<div class="home-section">

## Writing

{% for post in site.posts limit:5 %}
- [{{ post.title }}]({{ post.url | relative_url }})
  <span class="post-meta">{{ post.date | date: "%B %Y" }}</span>
{% endfor %}

</div>
