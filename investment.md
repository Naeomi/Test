---
layout: default

title: Investment
category: investment
---

{% assign posts = site.tags[page.category] %}
{% include posts.html posts=posts %}
