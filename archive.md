---
layout: page
title: Archive


<h1>Archive of posts from {{ page.date | date: "%Y" }}</h1>

<ul class="posts">
{% for post in page.posts %}
  <li>
    <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
----

{% for post in site.posts %}
{% capture currentyear %}{{ post.date | date: "%Y. %m" }}{% endcapture %}
{% if currentyear != year %}

  <h1>{{ currentyear }}</h1>
    {% capture year %}{{ currentyear }}{% endcapture %}
  {% endif %}

  <li>{{ post.date | date: "%m. %d" }} — <a href="{{ post.url }}">{{ post.title }}</a></li>

{% endfor %}
