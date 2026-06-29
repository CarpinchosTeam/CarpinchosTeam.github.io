---
layout: base
title: Noticias
permalink: /posts/
---

<style>
  .custom-hover {
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .custom-hover:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.08) !important;
  }
</style>

<main class="container-md mt-5 pt-5 pb-5">
  <div class="row">
    <div class="col-lg-10 offset-lg-1">
      <div class="text-center mb-5 mt-3">
        <h1 class="display-4 fw-bold mb-4" style="letter-spacing: -1px;">Noticias</h1>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
        <p class="lead text-muted mt-4 mb-0" style="font-size: 1.3rem;">Todas las novedades del Equipo Carpinchos</p>
      </div>

      <div class="row">
        {% for post in site.posts %}
        <div class="col-md-6 mb-4">
          <div class="card h-100 bg-white p-4 shadow-sm border-0 rounded-lg custom-hover">
            <span class="text-uppercase fw-bold mb-2" style="font-size: 0.8rem; letter-spacing: 1px; color: var(--accent);">
              {{ post.date | date: "%d/%m/%Y" }}
            </span>
            <h4 class="fw-bold mb-3"><a href="{{ post.url | relative_url }}" class="text-decoration-none text-dark">{{ post.title }}</a></h4>
            <p class="text-muted mb-4 mt-0">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
            <div class="mt-auto">
              <a href="{{ post.url | relative_url }}" class="fw-bold text-primary text-decoration-none" style="font-size: 0.9rem;">Leer más <i class="fa-solid fa-arrow-right ml-1"></i></a>
            </div>
          </div>
        </div>
        {% endfor %}
      </div>
    </div>
  </div>
</main>
