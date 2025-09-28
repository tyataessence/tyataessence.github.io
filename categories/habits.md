---
layout: category
title: "Habits"
category: Habits
permalink: /categories/habits/
---

Welcome to the **Insights** category! Here you'll find posts about habits, life experiences, productivity, and thoughts that I want to share with my readers.

This section is meant to simplify ideas and provide insights on habits applicable to daily life, mental growth, and self-improvement.

Below is a list of all posts in the Habits category:

{% assign habits_posts = site.categories.Habits | sort: 'date' | reverse %}

<ul>
  {% for post in habits_posts %}
    <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%b %d, %Y" }}</li>
  {% endfor %}
</ul>
