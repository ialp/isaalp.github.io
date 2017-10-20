---
layout: page
title: Archive
----





{% for post in site.posts %}
{% capture currentyear %}{{ post.date | date: "%Y. %m" }}{% endcapture %}
{% if currentyear != year %}

  <h1>{{ currentyear }}</h1>
    {% capture year %}{{ currentyear }}{% endcapture %}
  {% endif %}
a2
  <li> <a href="{{ post.url }}">{{ post.title }}</a>   -  <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span> </li>
      

{% endfor %}
