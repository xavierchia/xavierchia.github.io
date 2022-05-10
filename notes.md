---
layout: page
title:
permalink: /notes/
---

I love reading books. But even more so I love studying how people a few steps ahead of me go to where they are now. After picking a new "target" I consume everything they've written, every podcast episode they appeared on, and spent hours researching what they actually do, not just what they say. 

Then I write about the patterns, ideas, and lessons I've learned from that and share them here. 

*Some of the notes are still work-in-progress.*


<div class="posts">
  {% for post in site.categories.notes %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>