---
layout: page
title: Links
permalink: /links/
---

<!-- {% include image.html url="/images/octojekyll.png" caption="Octojekyll." width=300 align="right" %} -->



On this page, I hope to list interesting links I find worthy of sharing: books, webpages or resources related to any of my interests: science, engineering, mathematics, music, photography, languages, travel or others.
<br><br>
<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  <!-- {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %} -->
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
