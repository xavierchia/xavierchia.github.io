---
title: 
published: true
layout: page
permalink: lists
excerpt: I started curating some of my favorite lists
image: /images/default.jpg
---

<div class="posts">


 <div class="posts">
  <article class="post">
    <p>⭐️ Essays I put serious effort into</p>
    <p>🧠 Raw brain dumps</p>
  </article>


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
    <a class="is-active" href="/lists" >Lists</a>
    </li>
    <li>
      <a  href="/notes" class="btn-nav">Book Notes</a>
    </li>
    <li>
      <a  href="/profiles" class="btn-nav" >Profiles</a>
    </li>
  </ul>
</div>

  

  

  {% for post in site.categories.lists %}
    <article class="post">
      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>
      <div class="entry">
        {{ post.excerpt }}
      </div>
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>


 <h1>Other People's Lists</h1>

* [Things you're allowed to do](https://milan.cvitkovic.net/writing/things_youre_allowed_to_do/)
* [Activities with (positive) asymmetric returns](https://blog.tjcx.me/p/activities-with-positive-asymmetric)
* [50 First Levers (How to start building Leverage)](https://www.ejorgenson.com/blog/50-first-levers)
* [140+ Examples of Atomic Habits](https://docs.google.com/spreadsheets/d/14oKKZ_MEy171WhvUe8OPzcCC53oKPWqEFEiAnN91_7A/edit#gid=0)
* [Bucket List by Philip Young](https://www.philipyoungg.com/bucket-list)
