---
layout: page
title: Vemcodex
description: Building high-quality high-ROI Software
---

Welcome to Vemcodex, your central source of high quality information to build great software and improve your team productivity.

{% for post in site.posts reversed %}
<h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
{% assign author = site.data.authors[post.author] %}

  <div class="date">
    Written by <a href="{{ author.web }}" target="_blank">{{ author.name }}</a> on {{ post.created | date: "%B %e, %Y" }}, last modified {{ post.modified | date: "%B %e, %Y" }}
  </div>
  
<hr/>
{{ post.excerpt }}
{% endfor %}
