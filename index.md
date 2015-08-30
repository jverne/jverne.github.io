---
title: Home
---

{% for post in site.posts limit:15 %}
## [{{ post.title }}]({{ post.url }})
_<time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_long_string }}</time>_

{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
---
{% endfor %}
