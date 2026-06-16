---
layout: default
title: Todos os Artigos
permalink: /artigos/
---

<section class="archive-header">
  <h1>Todos os Artigos</h1>
  <p class="archive-count">{{ site.posts | size }} publicações</p>
</section>

<section class="archive-list">
  {% for post in site.posts %}
    <article class="archive-item">
      <div style="display:flex;gap:24px;align-items:start">
        <img src="{{ post.image | relative_url }}" alt="" style="width:140px;height:100px;object-fit:cover;flex-shrink:0">
        <div>
          <div class="archive-meta">
            <time>{{ post.date | date: "%d/%m/%Y" }}</time>
            <span class="section-tag">{{ post.categories | first | default: "artigo" }}</span>
          </div>
          <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
          <p class="archive-author">{{ post.author }}</p>
        </div>
      </div>
    </article>
  {% endfor %}
</section>