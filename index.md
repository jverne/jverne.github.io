---
title: Home
---

{% for post in site.posts limit:15 %}
{% assign post_category = post.categories | first %}
<h2>{% include category_icon.html category=post_category iconsize="large" %} <a href="{{ post.url }}">{{ post.title }}</a></h2>
_<time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%a, %d %b %Y %R %Z" }}</time>_

{{ post.excerpt | remove: '<p>' | remove: '</p>' }}

{% assign full_length = post.content | strip_html | strip_newlines | size %}
{% assign excerpt_length = post.excerpt | strip_html | strip_newlines | size %}
{% if full_length > excerpt_length %}
[<i class="fa fa-ellipsis-h" title="Open '{{ post.title}}'"></i>]({{ post.url }})
{% endif %}

{% unless forloop.last %}---{% endunless %}
{% endfor %}
