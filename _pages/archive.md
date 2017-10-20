---
layout: page
title: Tüm Yazılar
permalink: /tum-yazilar/
---


isaalp.com’da yayınlanan tüm yazılar, altta listelenmiştir.




 <ul class="post-list">
    {% for post in site.posts %}
     <a href="{{ post.url | prepend: site.baseurl }}">
     
     <li class="post-box">
         <span class="post-meta"><strong>{{ post.date | date: "%-d" }}</strong><br />{{ post.date | date: "%b" }}</span>
         <h2 class="post-link">{{ post.title }}</h2>
      </li></a>
    {% endfor %}
  </ul>
