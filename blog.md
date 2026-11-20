---
layout: default
title: Blog
permalink: /blog/
description: Follow the build.
---

<section class="blog-index">
  <h1 class="blog-index__title">Follow the build</h1>

  {% if site.posts.size > 0 %}
    <ul class="blog-index__posts">
      {% for post in site.posts %}
        <li class="blog-index__post">
          <time class="blog-index__date" datetime="{{ post.date | date_to_xmlschema }}">
            {{ post.date | date: "%b %-d, %Y" }}
          </time>
          <a class="blog-index__link" href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </li>
      {% endfor %}
    </ul>
  {% else %}
    <p class="blog-index__empty">No posts yet.</p>
  {% endif %}
</section>
