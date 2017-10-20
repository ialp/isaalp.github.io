---
layout: page
title: Tüm Yazılar
permalink: /tum-yazilar/
---


isaalp.com’da yayınlanan tüm yazılar, altta listelenmiştir.



<div class="item {% if post.star %}star{% endif %}">
    <a class="url" href="{{ site.url }}{{ post.url }}">
        <aside class="date"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d %Y" }}</time></aside>
        <h3 class="title">{{ post.title }}</h3>
    </a>
</div>
