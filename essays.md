---
layout: page
title: Essays
permalink: /essays/
---



## 0 to 0.1 - a humble path to financial independence

- [The dawn of the humble age](/dawn)
- [The humble creator manifesto](/manifesto)

Part 1: Ideation

- [Humble business ideas - an introduction](/humble_introduction)
- [How to come up with humble business ideas?](/ideation)
- [How to quantify the potential of humble business ideas](/quantify)
- [Humble Businesses vs. Startups](/humble_vs_startups)
- [The humble businesses hyperspace](/hyperspace)

Part 2: Execution

- [How to create a humble personal brand](/humble_brand)


##No-Nonsense Muscle Training - a scientific guide for normal people##

- [Taking a Scientific Approach to Muscle Training](/scientific)
- [Why care about weightlifting?](/why-care)

Part 1: What Everybody Ought to Know About Weightlifting

- [Bird's-Eye View of Effective Weightlifting](/bird)



## Most Recent Essays

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Read More</a>
    </article>
  {% endfor %}
</div>