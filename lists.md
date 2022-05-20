---
title: 
published: true
layout: page
permalink: lists
excerpt: I started curating some of my favorite lists
image: /images/default.jpg
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
    <a class="is-active" href="/lists" >Lists</a>
    </li>
    <li>
      <a  href="/notes" class="btn-nav">Book Notes</a>
    </li>
    <li>
      <a  href="/profiles" class="btn-nav" >Permissionless Mentors</a>
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


<article class="post">
 <h1>Other People's Lists</h1>

 <ul>
  <li><a href="https://milan.cvitkovic.net/writing/things_youre_allowed_to_do">Things you're allowed to do</a></li>
  <li><a href="https://blog.tjcx.me/p/activities-with-positive-asymmetric">Activities with (positive) asymmetric returns</a></li>
  <li><a href="https://www.ejorgenson.com/blog/50-first-levers">50 First Levers (How to start building Leverage</a></li>
  <li><a href="https://docs.google.com/spreadsheets/d/14oKKZ_MEy171WhvUe8OPzcCC53oKPWqEFEiAnN91_7A/edit#gid=0">140+ Examples of Atomic Habits</a></li>
  <li><a href="https://www.philipyoungg.com/bucket-list">Bucket List by Philip Young</a></li>
 </ul>


</article>
