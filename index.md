---
title: Home
---

{% for post in site.posts limit:15 %}
## [{{ post.title }}]({{ post.url }})
_<time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%c" }}</time>_

{{ post.excerpt | remove: '<p>' | remove: '</p>' }}

{% assign full_length = post.content | strip_html | strip_newlines | size %}
{% assign excerpt_length = post.excerpt | strip_html | strip_newlines | size %}
{% if full_length > excerpt_length %}
[<i class="fa fa-ellipsis-h" title="Open '{{ post.title}}'"></i>]({{ post.url }})
{% endif %}

{% unless forloop.last %}---{% endunless %}
{% endfor %}
