---
layout: page
title: Tüm Yazılar
permalink: /tum-yazilar/
---


isaalp.com’da yayınlanan tüm yazılar, altta listelenmiştir.



{% for post in site.posts %}
{% capture currentyear %}{{ post.date | date: "%Y. %m" }}{% endcapture %}
{% if currentyear != year %}

  <h1>{{ currentyear }}</h1>
    {% capture year %}{{ currentyear }}{% endcapture %}
  {% endif %}

  <li>{{ post.date | date: "%m. %d .%Y" }} — <a href="{{ post.url }}">{{ post.title }}</a> </li>

{% endfor %}



                    
