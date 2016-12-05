---
layout: page
title: Posts Index
---

<div class="posts">
    {% for post in site.posts | sort: 'date', 'first' %}
        <div>
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {% for tag in post.tags | sort %}
            #{{ tag }}
        {% endfor %}
        </div>
    {% endfor %}
</div>

<div>
    {% for post in site.posts | sort: 'date', 'first' %}
        <div>
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {% for tag in post.tags | sort %}
            #{{ tag }}
        {% endfor %}
        </div>
    {% endfor %}
</div>