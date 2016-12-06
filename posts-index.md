---
layout: page
title: Posts Index
---

<div class="posts">
    {% for post in site.posts reversed %}
        <div class="index-post">
            <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
            ({{ post.date | date_to_string }})
            {% for tag in post.tags | sort %}
                <a href="{{site.url}}/tag-cloud.html#{{tag}}">#{{tag}}</a>
            {% endfor %}
        </div>
    {% endfor %}
</div>