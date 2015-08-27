---
title: Home
---

{% for post in site.posts limit:15 %}
## [{{ post.title }}]({{ post.url }})
{{ post.excerpt | remove: '<p>' | remove: '</p>' }}
---
{% endfor %}
