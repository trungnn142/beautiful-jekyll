---
layout: page
title: Linux Unix Tips
---

<div class="posts-list">
  {% for post in site.tags.linux %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	    <h2 class="post-title">{{ post.title }}</h2>

	    {% if post.subtitle %}
	    <h3 class="post-subtitle">
	      {{ post.subtitle }}
	    </h3>
	    {% endif %}
    </a>

    <span class="post-meta">
      {{ post.date | date: "%d-%m-%Y" }}
    </span>

    {% if post.tags.size > 0 %}
    <div class="blog-tags blog-tags--inline">
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tags#{{- tag -}}">{{- tag -}}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}
  </article>
  {% endfor %}
</div>
