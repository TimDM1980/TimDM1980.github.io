---
layout: page
title: Posts Index
---

v1

<div class="posts">
    {% for post in site.posts | sort: 'date', 'first' %}
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {% for tag in post.tags | sort %}
        <span class="site-tag">
            #{{ tag[0] }}
        </span>
        {% endfor %}
    {% endfor %}
</div>



todo: categories
todo: styling