---
layout: default
title: Winging It - All Posts
---

<div id="home">
  <h2>All Posts</h2>
  <ul>
    {% for post in site.posts %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
  <h2>Posts by Category</h2>
  <ul>
    {% for category in site.categories %}
      <li><a name="{{ category | first }}">{{ category | first }}</a>
        <ul>
        {% for posts in category %}
          {% for post in posts %}
            <li><a href=".{{ post.url }}">{{ post.title }}</a></li>
          {% endfor %}
        {% endfor %}
        </ul>
        <br/>
      </li>
    {% endfor %}
  </ul>
</div>
