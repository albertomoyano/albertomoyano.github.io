---
layout: page
title: Novedades
permalink: /blog/
---

# Últimos artículos

{% for post in site.posts limit:10 %}
   <div class="post-preview">
   <h2><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
   <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span><br>
   {% if post.badges %}{% for badge in post.badges %}<span class="badge badge-{{ badge.type }}">{{ badge.tag }}</span>{% endfor %}{% endif %}
   {{ post.content | split:'<!--more-->' | first }}
   {% if post.content contains '<!--more-->' %}
      <a href="{{ site.baseurl }}{{ post.url }}">seguir leyendo</a>
   {% endif %}
   </div>
   <hr>
{% endfor %}

También puede ver el <a href="{{ site.baseurl }}/archive/">historial de artículos</a>.
