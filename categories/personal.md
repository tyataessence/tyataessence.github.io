---
layout: category
title: "Personal"
category: Personal
permalink: /personal/
---

Welcome to the **Personal** category! Here you'll find posts about reflections, life experiences, productivity, and thoughts that I want to share with my readers.  

This section is meant to simplify ideas and provide insights from daily life, personal projects, and self-improvement.

Below is a list of all posts in the Personal category:

{% assign personal_posts = site.categories.Personal | sort: 'date' | reverse %}
<ul>
  {% for post in personal_posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%b %d, %Y" }}</li>
  {% endfor %}
</ul>
