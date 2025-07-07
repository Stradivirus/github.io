---
layout: default
title: "모든 포스트"
---

# 모든 포스트

<div class="posts-archive">
  {% for post in site.posts %}
    <div class="post-item">
      <h3>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      </h3>
      <p class="post-meta">
        <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y년 %m월 %d일" }}</time>
        {% if post.categories.size > 0 %}
          • 
          {% for category in post.categories %}
            <span class="category">{{ category }}</span>{% unless forloop.last %}, {% endunless %}
          {% endfor %}
        {% endif %}
      </p>
      <p>{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
    </div>
  {% endfor %}
</div>

<style>
.posts-archive {
  max-width: 800px;
  margin: 0 auto;
}

.post-item {
  margin-bottom: 2rem;
  padding-bottom: 1.5rem;
  border-bottom: 1px solid #eee;
}

.post-item h3 {
  margin: 0 0 0.5rem 0;
}

.post-item h3 a {
  color: #2c3e50;
  text-decoration: none;
}

.post-item h3 a:hover {
  color: #3498db;
}

.post-item .post-meta {
  color: #666;
  font-size: 0.9rem;
  margin: 0 0 1rem 0;
}

.post-item p {
  margin-bottom: 0;
  color: #555;
}
</style>
