---
layout: page
title: Posts Index
---

{% for post in site.posts %}
    <a href="{{ post.url }}">
    {{ post.title }}
    </a>

    <span class="post-date">{{ post.date | date_to_string }}</span>

{% endfor %}

todo: sort by date
todo: for each post: title, tags, categories
todo: styling