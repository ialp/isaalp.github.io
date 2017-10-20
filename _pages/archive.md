---
layout: page
title: Archive
permalink: /archive/
---



<section class="archive-post-list">

   {% for post in site.posts %}
       {% assign currentDate = post.date | date: "%Y" %}
       {% if currentDate != myDate %}
           
       {% endif %}
   {% endfor %}

</section>

----



{% for post in site.posts %}
{% capture currentyear %}{{ post.date | date: "%Y. %m" }}{% endcapture %}
{% if currentyear != year %}

  <h1>{{ currentyear }}</h1>
    {% capture year %}{{ currentyear }}{% endcapture %}
  {% endif %}

  <li>{{ post.date | date: "%m. %d" }} — <a href="{{ post.url }}">{{ post.title }}</a></li>

{% endfor %}
