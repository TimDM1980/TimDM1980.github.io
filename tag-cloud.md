---
layout: page
title: Tag Cloud
---

{% assign tags = site.tags | sort %}

{% for tag in tags %}
<span class="site-tag">
    <a href="/tag-cloud.html#{{ tag | first | slugify }}"
        style="font-size: {{ tag | last | size  |  times: 4 | plus: 80  }}%">
            {{ tag[0] | replace:'-', ' ' }} ({{ tag | last | size }})
    </a>
</span>
{% endfor %}


<div>
    {% for tag in tags %}
        <div>
    
        <a id="{{ tag | first | slugify }}">
            Posts with tag {{tag[0]}}
        </a>

        {% for post in site.tags[tag[0]] %}
            <a href="{{ post.url }}">{{ post.title }}</a> <br/>
        {% endfor %}
        
        </div>
    {% endfor %}
</div>