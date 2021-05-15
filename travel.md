---
layout: home
title: Travel
category: travel

regions:
- title: Africa
  sub: 
  - title: Zambia
    tag: zambia
- title: Americas
- title: Asia
  sub:
  - title: Hong Kong
    tag: hongkong
- title: Australasia
  sub: 
  - title: New Zealand
    tag: newzealand
- title: Europe

---

<div class="container map-container" style="height: 300px;">
  <iframe src="https://maps.google.com/maps?center=17.9187655,66.4819598&t=&z=2&ie=UTF8&iwloc=&output=embed" frameborder="0" style="border:0; width:100%; height:300px;" loading="lazy" allowfullscreen></iframe>
</div>

{% for region in page.regions %}
<h1>{{region.title}}</h1>
{% for sub in region.sub %}
<h2>{{sub.title}}</h2>

{% assign posts = site.tags[sub.tag] %}
{% include posts.html posts=posts %}

{% endfor %}
{% endfor %}
