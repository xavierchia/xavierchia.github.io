---
layout: page
title: 
permalink: /essays/
---

<div class="posts">
  <article class="post">
    <p>⭐️ Essays I put serious effort into</p>
    <p>🧠 Raw brain dumps</p>
  </article>


<div class="cat-nav">
  <ul>
    <li>
      <a class="is-active" href="/essays">Show All</a>
    </li>
    <li>
    <a href="/entrepreneurship" class="btn-nav">Entrepreneurship</a>
          </li>
    <li>
      <a href="/inner-game" class="btn-nav">Inner Game</a>
    </li>
    <li>
      <a href="/personal-brand-building" class="btn-nav">Personal Brand Building</a>
    </li>
        <li>
    <a href="/lists" class="btn-nav">Lists</a>
          </li>
    <li>
      <a href="/notes" class="btn-nav">Book Notes</a>
    </li>
    <li>
      <a href="/profiles" class="btn-nav">Profiles</a>
    </li>
  </ul>
</div>

  

  {% for post in site.posts %}
  <!-- {% unless post.categories contains "notes" or post.categories contains "lists"%} -->
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  <!-- {% endunless %} -->
  {% endfor %}
</div>