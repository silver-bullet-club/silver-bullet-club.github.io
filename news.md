---
layout: page
title: お知らせ一覧

---

<ul class="list-unstyled d-none d-sm-block">
  {% for post in site.posts %}
  <li class="media mb-3 border p-3 position-relative">
    <img src="{{ post.image }}" alt="" class="img-fluid mr-5" width="210">
    <div class="media-body">
      <h4 class="mt-0 mb-1">{{ post.title }}</h4>
      <small>{{ post.date | date_to_string }}</small>
      <p>
        {{ post.description }}
      </p>
      <a class="stretched-link" href="{{ post.url }}">記事を読む</a>
    </div>
  </li>
  {% endfor %}
</ul>

<div class="card-deck d-sm-none">
  {% for post in site.posts %}
  <div class="card">
    <img src="{{ post.image }}" alt="" class="card-img-top">
    <div class="card-body">
      <h5 class="card-title">{{ post.title }}</h5>
      <span class="card-subtitle text-muted">{{ post.date | date_to_string }}</span>
      <p class="card-text">
        {{ post.description }}
      </p>
      <a class="stretched-link" href="{{ post.url }}">記事を読む</a>
    </div>
  </div>
  {% endfor %}
</div>