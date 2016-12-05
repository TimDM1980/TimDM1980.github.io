---
layout: page
title: Posts Index
---

<div class="posts">
    {% for post in site.posts | sort: 'date', 'first' %}
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {% for tag in site.tags | sort %}
        <span class="site-tag">
            #{{ tag[0] }}
        </span>
        {% endfor %}
        {{ page.tags | array_to_sentence_string: 'or' }}
    {% endfor %}
</div>

<div>
    {% for post in site.posts | sort: 'date', 'first' %}
        <div class="post">
        <a href="{{ post.url }}">{{ post.title }}</a>
        ({{ post.date | date_to_string }})
        {{ page.tags | array_to_sentence_string: '' }}
        </div>
    {% endfor %}
</div>

todo: sort by date
todo: for each post: title, tags, categories
todo: styling