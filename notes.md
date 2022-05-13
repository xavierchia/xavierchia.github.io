---
layout: page
title:
permalink: /notes/
---


<div class="posts">



<div class="cat-nav">
  <ul>
    <li>
      <a  href="/essays">Show All</a>
    </li>
    <li>
    <a  href="/entrepreneurship" class="btn-nav">Entrepreneurship</a>
          </li>
    <li>
      <a  href="/inner-game" class="btn-nav">Inner Game</a>
    </li>
    <li>
      <a  href="/personal-brand-building" class="btn-nav">Personal Brand Building</a>
    </li>
    <li>
    <a href="/lists" class="btn-nav">Lists</a>
    </li>
    <li>
      <a class="is-active" href="/notes">Book Notes</a>
    </li>
    <li>
      <a href="/profiles" class="btn-nav">Profiles</a>
    </li>
  </ul>
</div>

  

  

  {% for post in site.categories.notes %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}

  <article class="post">
  <h1>Legend</h1>
    <p>⭐️ Essays I put serious effort into</p>
    <p>🧠 Raw brain dumps</p>
  </article>
</div>

