---
layout: page
title: Posts Index
---

<div class="posts">
    {% for post in site.posts | sort %}
        <a href="{{ post.url }}">
        {{ post.title }}
        </a>

        <span class="post-date">{{ post.date | date_to_string }}</span>

    {% endfor %}
</div>

<div class="posts">
  {% for post in site.posts | sort: 'date' %}
  <div class="post">
    <a href="{{ post.url }}">
    {{ post.title }}
    </a>

    <span class="post-date">{{ post.date | date_to_string }}</span>
  </div>
  {% endfor %}
</div>

todo: sort by date
todo: for each post: title, tags, categories
todo: styling