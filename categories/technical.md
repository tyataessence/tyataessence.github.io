---
layout: category
title: "Technical"
category: Technical
permalink: /categories/technical/
---

Welcome to the **Technical** category! Here you'll find posts about programming, development tools, GitHub, Jekyll, and other technology-related topics.

Whether you're a beginner or an experienced developer, these posts aim to simplify complex technical ideas and provide practical guidance.

Below is a list of all posts in the Technical category:

{% assign tech_posts = site.categories.Technical | sort: 'date' | reverse %}

<ul>
  {% for post in tech_posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%b %d, %Y" }}</li>
  {% endfor %}
</ul>
