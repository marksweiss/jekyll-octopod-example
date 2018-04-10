---
title: All Episodes 
layout: default
navigation: 1
order: 2
---
{% assign post = '' %}
{% assign current_post = '' %}
{% for p in site.posts -%}
  {% if post == '' and p.post_type == 'pod' %} 
    {% assign post = p %}
  {% endif %}
  {% if current_post == '' and p.post_type == 'pod' %} 
    {% assign current_post = p %}
  {% endif %}
{% endfor %}

{% include post.html %}

{% for post in site.posts -%}
  {% if post.post_type == 'pod' and post.url != current_post.url -%}
    {% include post_line.html %}
  {% endif %}
{% endfor %}
