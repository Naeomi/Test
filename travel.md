---
layout: home
title: Travel
category: travel
---

{% assign posts = site.tags[page.category] %}
{% include posts.html posts=posts %}
