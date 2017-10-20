---
layout: page
title: Tüm Yazılar
permalink: /tum-yazilar/
---


isaalp.com’da yayınlanan tüm yazılar, altta listelenmiştir.




<ul class="post-list">
    {% for post in paginator.posts %}
      <li>
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          <span class="post-meta"><small>{{ post.date | date: "%b %-d, %Y" }}</small></span>
        </h2>
         
      </li>

    {% endfor %}
  </ul>
