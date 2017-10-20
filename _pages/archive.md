---
layout: page
title: Tüm Yazılar
permalink: /tum-yazilar/
---


isaalp.com’da yayınlanan tüm yazılar, altta listelenmiştir.



<div class="archive">
  <div class="timeline" id="timeline">
    {% for post in site.posts %}
    {% unless post.next %}
    <div class="archive-title">
      <h4 class="archive-year">{{ post.date | date: '%Y' }}</h4>
    </div>

    <ul>
    {% else %}
      {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
      {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
    {% if year != nyear %}
    </ul>
    <div class="archive-title">
      <h4 class="archive-year">{{ post.date | date: '%Y' }}</h4>
    </div>

    <ul>
    {% endif %}
    {% endunless %}
    <li>
       <a href="{{ site.url }}{{ post.url }}">{{ post.title }}</a>    - {{ post.date | date: "%d %b %Y" }}</li>  
    {% endfor %}
    </ul>

  </div>
