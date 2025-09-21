---
layout: default
title: "How to create free portfolio and blogsite using github."
date: 2025-09-21
categories: [Technical]
tags: [portfolio, blogsite, Technical]
author: Rakesh Tyata
---

## Why create portfolio and blogsite?

In tech industry, we often talk about **technical debts**, when engineering systems and practices are outdated or stagnant, failing to evolve with time. Similarly, in life, staying stuck in old habits or mindsets can hold us back. To grow and stay relevant, we must continously learn and adopt new approaches and practices. One effective way to do this and distinguish yourself is by creating a portfolio and a blogsite.

- A portfolio helps to highlight your work samples, projects and accomplishments demonstrating your skills.
- A blogsite helps to capture and share your posts on tech tutorials, coding guides, trending standards and topics demonstrating your learnings and interest.

- This repository is designed as a **personal portfolio website**.
- Showcases professional background, technical skills, and projects.
- Built using **Jekyll**, a static site generator:
- Processes Markdown files and templates to generate static HTML pages.
- Does not require a backend server.
- Lightweight, fast-loading, and easy to maintain.

## Prerequisite Fundamentals

- **Markdown:** A lightweight markup language to format text (headings, lists, links) easily. Learn more: https://www.markdownguide.org
- **GitHub:** A platform for version control and hosting code repositories online. Learn more: https://docs.github.com/en/get-started/quickstart
- **HTML:** The standard language to create and structure web pages. Learn more: https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS:** A language used to style HTML elements and design web pages. Learn more: https://developer.mozilla.org/en-US/docs/Web/CSS

## How to create portfolio in github?

---

- Sign up for a free GitHub account for specific username. This will generate your GitHub Page URL (https://username.github.io).
- Create a new repository named username.github.io, to host your portfolio website.
- Add README.md to your repository. Use Markdown to highlight your portfolio contents: skills, work experiences and education.
- Add_config file to your repository. Use **Jekyll** theme, a static site generator that converts Markdown files and templates into static HTML pages.
- Include a profile picture and other visual elements to make your portfolio attractive and engaging.

**Sample Portfolio Structure**

```
rtyata01.github.io/
├── _config.yml
├── assets/
│   └── img/
│       └── profile_pic.jpg
└── README.md

```

**Sample blogsite Structure**

```
tyataessence.github.io/
├── _includes/
│   ├── footer.html
│   └── sidebar.html
├── _layouts/
│   ├── category.html
│   ├── default.html
│   └── home.html
├── _posts/
│   ├── personal/
│   │   └── 2025-09-21-why-tyata-essence.md
│   ├── technical/
│   │   └── 2025-09-21-create-portfolio-blogsite.md
│   └── trending/
│   │   ├── 2025-09-16-tips-for-blogging.md
│   │   └── 2025-09-21-artificial-intelligence.md
├── assets/
│   ├── images/
│   │   ├── banner.jpg
│   │   └── profile_pic.jpg
│   └── styles/
│       ├── banner.css
│       ├── footer.css
│       ├── layout.css
│       └── sidebar.css
├── categories/
│   ├── personal.md
│   ├── technical.md
│   └── trending.md
├── _config.yml
└── index.md
```
