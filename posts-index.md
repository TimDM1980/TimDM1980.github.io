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
            #{{ tag }}
        {% endfor %}
    {% endfor %}
</div>

<div>
    {% for post in site.posts | sort: 'date', 'first' %}
        <div class="post">
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        #{{ post.tags | array_to_sentence_string: '' }}
        </div>
    {% endfor %}
</div>

todo: categories
todo: styling