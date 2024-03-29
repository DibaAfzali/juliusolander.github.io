---
layout: page
title: Assignment 2
permalink: /assignment-2/
---

# Assignment 2

Welcome to Assignment 2. This page will have a custom magazine-style layout.
/* Container for your articles */
.articles-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

/* Individual article cards */
.article-card {
  border: 1px solid #ccc;
  border-radius: 5px;
  overflow: hidden;
}

.article-card img {
  width: 100%;
  height: auto;
}

.article-card-content {
  padding: 15px;
}

.article-title {
  font-size: 20px;
  margin-bottom: 10px;
}
<div class="articles-grid">
  {% for post in site.posts %}
    <div class="article-card">
      <img src="{{ post.image }}" alt="{{ post.title }}">
      <div class="article-card-content">
        <h2 class="article-title">{{ post.title }}</h2>
        <p>{{ post.excerpt }}</p>
      </div>
    </div>
  {% endfor %}
</div>
