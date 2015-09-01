---
title: Archive
---

# {{ page.title }}
{% for post in site.posts %}
- {{ post.date | date_to_long_string }} &middot; [{{ post.title }}]({{ post.url }})
{% endfor %}