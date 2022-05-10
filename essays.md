---
layout: page
title: 
permalink: /essays/
---

<div class="posts">
  {% for post in site.posts %}
  {% unless post.categories contains "notes"%}
  {% unless post.categories contains "lists"%}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endunless %}
  {% endunless %}
  {% endfor %}
</div>