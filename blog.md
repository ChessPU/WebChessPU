---
layout: default
title: chessPU - Blog
---
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.date | date_to_long_string }} - {{ post.title }}</a>       
       {% include blog/blog-card.html %}             
    </li>
    <br><br>
  {% endfor %}
</ul>