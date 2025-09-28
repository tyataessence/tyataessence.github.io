---
layout: category
title: "Career"
category: Career
permalink: /categories/career/
---

Welcome to the **Career** category! Here you'll find posts about reflections about career, life experiences, productivity, and thoughts that I want to share with my readers.

This section is meant to simplify ideas and provide career insights, learnings, mental growth, and self-improvement.

Below is a list of all posts in the Career category:

{% assign career_posts = site.categories.Career | sort: 'date' | reverse %}

<ul>
  {% for post in career_posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%b %d, %Y" }}</li>
  {% endfor %}
</ul>
