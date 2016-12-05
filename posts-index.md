---
layout: page
title: Posts Index
---

<div>
    {% for post in site.posts | sort: 'date', 'first' %}
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {% for tag in site.tags | sort %}
        <span class="site-tag">
            {{ tag[0] | replace:'-', ' ' }}
            #{{ tag[0] }}
        </span>
        {% endfor %}
    {% endfor %}
</div>

todo: sort by date
todo: for each post: title, tags, categories
todo: styling