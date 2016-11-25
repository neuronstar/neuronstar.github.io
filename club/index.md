---
title: Reading Club
layout: page
excerpt: Reading Club
search_omit: true
---

## List of Reading Clubs
{:.no_toc}

* Categories
{:toc}


## Spiking Neuron Models Reading Club

<ul class="post-list">
{% assign snm = site.spiking-neuron-models | sort: 'title' %}
{% for post in snm %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.author }}"> by &nbsp; {{ post.author }}</time></span>
  {% if post.summary %} <span class="excerpt">{{ post.summary | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>
  {% else post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
