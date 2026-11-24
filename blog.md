---
layout: default
title: Blog
permalink: /blog/
description: A chronicle of the Chalk World build.
---

<section class="page-head">
  <div class="wrap">
    <p class="section-label">The blog</p>
    <h1 class="page-head__title">Follow the build</h1>
    <p class="page-head__lede">
      A chronicle of building Chalk World. Engineering notes,
      architectural decisions, dead ends, and the occasional essay
      about why any of this.
    </p>
  </div>
</section>

<section class="block" style="padding-top: 0; border-top: none;">
  <div class="wrap">
    {% assign pinned_posts = site.posts | where: "pinned", true %}
    {% assign unpinned_posts = site.posts | where_exp: "p", "p.pinned != true" %}

    {% if site.posts.size > 0 %}
    <ul class="blog-list">
      {% for post in pinned_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
          <div>
            <span class="blog-list__chip blog-list__chip--pinned">Start here</span>
            <h2 class="blog-list__title">{{ post.title }}</h2>
            {% if post.description %}
            <p class="blog-list__excerpt">{{ post.description }}</p>
            {% elsif post.excerpt %}
            <p class="blog-list__excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
            {% endif %}
          </div>
        </a>
      </li>
      {% endfor %}

      {% for post in unpinned_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%b %-d, %Y" }}</time>
          <div>
            <h2 class="blog-list__title">{{ post.title }}</h2>
            {% if post.description %}
            <p class="blog-list__excerpt">{{ post.description }}</p>
            {% elsif post.excerpt %}
            <p class="blog-list__excerpt">{{ post.excerpt | strip_html | truncate: 160 }}</p>
            {% endif %}
          </div>
        </a>
      </li>
      {% endfor %}
    </ul>
    {% else %}
    <p>No posts yet.</p>
    {% endif %}
  </div>
</section>