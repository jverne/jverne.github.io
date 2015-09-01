---
title: Categories
---

# {{ page.title }}

<!-- Ripped wholesale from https://github.com/LanyonM/lanyonm.github.io/blob/master/tags.html -->

{% capture site_categories %}{% for category in site.categories %}{{ category | first }}{% unless forloop.last %},{% endunless %}{% endfor %}{% endcapture %}
<!-- site_categories: {{ site_categories }} -->
{% assign category_word = site_categories | split:',' | sort %}
<!-- category_word: {{ category_word }} -->

<div id="categories">
  <ul class="inline">
  {% for item in (0..site.categories.size) %}{% unless forloop.last %}
    {% capture this_word %}{{ category_word[item] | strip_newlines }}{% endcapture %}
    <li class="inline"><a href="#{{ this_word | cgi_escape }}">{{ this_word }} <span class="super w3-yellow">{{ site.categories[this_word].size }}</span></a></li>
  {% endunless %}{% endfor %}
  </ul>

  {% for item in (0..site.categories.size) %}{% unless forloop.last %}
    {% capture this_word %}{{ category_word[item] | strip_newlines }}{% endcapture %}
  <h2 id="{{ this_word | cgi_escape }}">{{ this_word }}</h2>
  <ul class="posts">
    {% for post in site.categories[this_word] %}{% if post.title != null %}
    <li itemscope><span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date_to_long_string }}</time></span> &middot; {% if post.category == "speaking" %}<i class="fa fa-microphone"></i> {% endif %}<a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endif %}{% endfor %}
  </ul>
  {% endunless %}{% endfor %}
</div>
