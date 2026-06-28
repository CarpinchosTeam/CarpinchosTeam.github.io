---
layout: base
title: Inicio
---

<!-- 1. HERO -->
<section class="hero-section text-center py-5 bg-primary text-white" style="background-image: url('{{ '/assets/img/hero-placeholder.jpg' | relative_url }}'); background-size: cover; background-position: center; position: relative; min-height: 80vh; display: flex; align-items: center;">
  <div style="background-color: rgba(3, 0, 42, 0.85); position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></div>
  <div class="container position-relative py-5" style="z-index: 1;">
    <img src="{{ '/assets/img/logo-carpincho.svg' | relative_url }}" alt="Carpinchos Logo" style="width: 220px; margin-bottom: 2.5rem; filter: drop-shadow(0 4px 6px rgba(0,0,0,0.3));">
    <h1 class="display-3 fw-bolder text-white mb-4" style="letter-spacing: -1px;">Equipo Carpinchos</h1>
    <p class="lead fw-normal mx-auto mb-5 text-light" style="max-width: 800px; font-size: 1.5rem; line-height: 1.6;">
      Somos el equipo de Computación de Alto Rendimiento de la Universidad Nacional de Córdoba.
    </p>
    <div class="d-flex justify-content-center gap-4 flex-wrap">
      <a href="#recorrido" class="btn btn-primary btn-lg px-5 shadow-lg">Conocé nuestra historia</a>
      <a href="#apoyanos" class="btn btn-outline-light btn-lg px-5">Apoyanos</a>
    </div>
  </div>
</section>

<div class="container-md mt-5">

  <!-- 2. ¿QUÉ HACEMOS? -->
  <section class="py-5" id="que-hacemos">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">¿Qué hacemos?</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    </div>
    <div class="row text-center mt-5">
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-primary">
          <i class="fa-solid fa-trophy" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">Competimos internacionalmente</h4>
        <p class="text-muted" style="font-size: 1.1rem;">Representamos a Argentina en las competencias de supercómputo más exigentes del mundo.</p>
      </div>
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-primary">
          <i class="fa-solid fa-graduation-cap" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">Formamos estudiantes</h4>
        <p class="text-muted" style="font-size: 1.1rem;">Capacitamos a la próxima generación de profesionales y científicos en computación de alto rendimiento.</p>
      </div>
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-primary">
          <i class="fa-solid fa-microchip" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">Desarrollamos tecnología</h4>
        <p class="text-muted" style="font-size: 1.1rem;">Creamos software, optimizamos algoritmos y diseñamos infraestructura para resolver problemas complejos.</p>
      </div>
    </div>
  </section>

  <!-- 3. ¿POR QUÉ HACEMOS ESTO? -->
  <section class="py-5 my-4" id="proposito">
    <div class="row justify-content-center">
      <div class="col-lg-9 text-center">
        <h2 class="display-5 fw-bold mb-4">Nuestro Propósito</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto 30px auto; border-radius: 2px;"></div>
        <p class="lead text-muted" style="font-size: 1.35rem; line-height: 1.8;">
          Las competencias internacionales no son un fin en sí mismo, sino una poderosa herramienta. Las utilizamos como motor para <strong class="text-dark">formar estudiantes de excelencia en HPC</strong>, desarrollar tecnologías de vanguardia y fortalecer la comunidad científica y tecnológica de nuestra región.
        </p>
      </div>
    </div>
  </section>

  <!-- 4. IMPACTO -->
  <section class="py-5 bg-white rounded-4 p-5 text-center shadow-sm my-5" id="impacto">
    <h2 class="display-5 fw-bold mb-5">El Impacto</h2>
    <div class="row mt-4">
      <div class="col-6 col-md-3 mb-4">
        <div class="impact-number">{{ site.competencias | size }}</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px;">Competencias<br>Internacionales</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <div class="impact-number">{{ site.integrantes | size }}</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px;">Estudiantes<br>Formados</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <div class="impact-number">{{ site.data.bancarpinchos | size }}</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px;">Bancarpinchos<br>Activos</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <div class="impact-number">3</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px;">Sponsors<br>Institucionales</p>
      </div>
    </div>
  </section>

  <!-- 5. COMPETENCIAS (Timeline) -->
  <section class="py-5 my-5" id="recorrido">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">Historia y Competencias</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
      <p class="lead text-muted mt-4">El archivo de nuestra participación en el mundo.</p>
    </div>
    
    <div class="timeline mt-5">
      {% assign comps_sorted = site.competencias | sort: "year" | reverse %}
      {% for comp in comps_sorted %}
      <div class="timeline-item">
        <div class="timeline-content">
          <div class="timeline-year">{{ comp.year }}</div>
          <h4 class="fw-bold mb-2"><a href="{{ comp.url | relative_url }}" class="text-decoration-none text-dark">{{ comp.name }}</a></h4>
          <p class="text-muted mb-2"><i class="fa-solid fa-location-dot me-2 text-primary"></i>{{ comp.location }}</p>
          {% if comp.award %}
          <div class="d-inline-block bg-light rounded-pill px-3 py-1 mb-3">
            <span class="text-primary fw-bold small ui-font"><i class="fa-solid fa-award me-2"></i>{{ comp.award }}</span>
          </div>
          {% endif %}
          <div class="mt-2">
            <a href="{{ comp.url | relative_url }}" class="fw-bold text-primary ui-font text-decoration-none" style="font-size: 0.9rem;">Ver detalles completos <i class="fa-solid fa-arrow-right ms-1"></i></a>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- 6. EQUIPO ACTUAL -->
  <section class="py-5 my-5 bg-white rounded-4 p-5 shadow-sm" id="equipo">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">El Equipo Actual</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    </div>
    
    <div class="row justify-content-center mt-5">
      {% assign current_members = site.integrantes | where: "status", 'current' %}
      {% for integrante in current_members %}
      <div class="col-6 col-md-4 col-lg-3 text-center mb-5">
        <a href="{{ integrante.url | relative_url }}" class="text-decoration-none">
          {% if integrante.github %}
          <img src="https://github.com/{{ integrante.github }}.png?size=150" alt="{{ integrante.name }}" class="rounded-circle mb-3 avatar-circle" style="width: 130px; height: 130px; object-fit: cover;">
          {% else %}
          <div class="rounded-circle mb-3 bg-secondary d-inline-block avatar-circle" style="width: 130px; height: 130px;"></div>
          {% endif %}
          <h5 class="fw-bold mb-1 text-dark">{{ integrante.name }}</h5>
          <p class="text-primary ui-font small fw-bold">{{ integrante.role }}</p>
        </a>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- 7. SPONSORS -->
  <section class="py-5 my-5 text-center" id="sponsors">
    <h2 class="display-5 fw-bold mb-3">Nuestros Sponsors</h2>
    <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    <p class="lead text-muted mt-4 mb-5">Instituciones y empresas que apuestan por el talento universitario.</p>
    
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap mt-5">
      <div class="text-center">
        <a href="https://inpunto.la/" target="_blank" class="text-decoration-none text-dark d-block card bg-white p-4" style="width: 220px; height: 120px; display: flex !important; align-items: center; justify-content: center;">
          <h3 class="m-0 fw-bold" style="letter-spacing: -1px;">InPunto</h3>
        </a>
        <p class="mt-3 text-muted fw-bold small text-uppercase ui-font">Sponsor Oro</p>
      </div>
      <div class="text-center">
        <a href="https://txpipe.io/" target="_blank" class="text-decoration-none text-dark d-block card bg-white p-4" style="width: 220px; height: 120px; display: flex !important; align-items: center; justify-content: center;">
          <h3 class="m-0 fw-bold" style="letter-spacing: -1px;">TxPipe</h3>
        </a>
        <p class="mt-3 text-muted fw-bold small text-uppercase ui-font">Sponsor Plata</p>
      </div>
      <div class="text-center">
        <a href="https://nerdearla.com/" target="_blank" class="text-decoration-none text-dark d-block card bg-white p-4" style="width: 220px; height: 120px; display: flex !important; align-items: center; justify-content: center;">
          <h3 class="m-0 fw-bold" style="letter-spacing: -1px;">Nerdearla</h3>
        </a>
        <p class="mt-3 text-muted fw-bold small text-uppercase ui-font">Sponsor Bronce</p>
      </div>
    </div>

    <div class="mt-5 pt-3">
      <a href="https://docs.google.com/presentation/d/1CdKjTrHeCHs50wEVKzI28m1R14SMBw_xwptN4yIPCAo/edit?slide=id.p#slide=id.p" target="_blank" class="btn btn-outline-primary">Convertirse en Sponsor <i class="fa-solid fa-arrow-up-right-from-square ms-2"></i></a>
    </div>
  </section>

  <!-- 8. BANCARPINCHOS -->
  <section class="py-5 my-5 bg-primary text-white rounded-4 p-5 shadow-lg" id="apoyanos" style="position: relative; overflow: hidden;">
    <div style="position: absolute; top: -50%; left: -10%; width: 50%; height: 200%; background: radial-gradient(circle, rgba(5,160,175,0.15) 0%, rgba(3,0,42,0) 70%); pointer-events: none;"></div>
    <div class="row align-items-center position-relative" style="z-index: 1;">
      <div class="col-lg-6 mb-5 mb-lg-0 pe-lg-5">
        <h2 class="display-4 fw-bold text-white mb-4">La comunidad que nos sostiene</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin-bottom: 30px; border-radius: 2px;"></div>
        <p class="lead mb-4" style="font-size: 1.25rem; line-height: 1.7; opacity: 0.9;">
          Más de {{ site.data.bancarpinchos | size }} personas apoyan económicamente al equipo y hacen posible que representemos a la Universidad Nacional de Córdoba en competencias internacionales. A ellos los llamamos <strong>Bancarpinchos</strong>.
        </p>
        <div class="mt-5">
          <a href="https://cafecito.app/teamcarpinchos" target="_blank" class="btn btn-light btn-lg text-primary ui-font px-4 py-3 shadow">
            <i class="fa-solid fa-mug-hot me-2"></i> Convertite en Bancarpincho
          </a>
        </div>
        <p class="mt-4 small ui-font" style="opacity: 0.7;">Alias ARS: teamcarpinchos &bull; Alias USD: teamcarpinchos.usd</p>
      </div>
      <div class="col-lg-6">
        <div class="bg-white text-dark rounded-4 p-4 p-md-5 shadow-lg">
          <div class="d-flex align-items-center mb-4 border-bottom pb-3">
            <i class="fa-solid fa-heart text-primary fs-3 me-3"></i>
            <h4 class="fw-bold m-0">¡Gracias Bancarpinchos!</h4>
          </div>
          <div class="bancarpinchos-list pe-3" style="max-height: 350px; overflow-y: auto;">
            <ul class="list-unstyled mb-0" style="column-count: 2; column-gap: 2rem;">
              {% for donor in site.data.bancarpinchos %}
              <li class="mb-3">
                <span class="d-block text-dark fw-bold ui-font" style="font-size: 0.95rem;">{{ donor.name }}</span>
              </li>
              {% endfor %}
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 9. NOTICIAS -->
  <section class="py-5 mt-5 border-top border-2" id="noticias" style="border-color: rgba(0,0,0,0.05) !important;">
    <div class="row align-items-center mb-5">
      <div class="col-md-8">
        <h3 class="display-6 fw-bold mb-0">Últimas Novedades</h3>
      </div>
      <div class="col-md-4 text-md-end mt-3 mt-md-0">
        <a href="{{ '/tags' | relative_url }}" class="btn btn-outline-primary btn-sm">Ver archivo de noticias</a>
      </div>
    </div>
    
    <div class="row">
      {% assign posts = site.posts %}
      {% for post in posts limit:3 %}
      <div class="col-md-4 mb-4">
        <div class="card h-100 bg-white p-4">
          <div class="text-primary ui-font small fw-bold mb-3"><i class="fa-regular fa-calendar me-2"></i>{{ post.date | date: "%d/%m/%Y" }}</div>
          <h5 class="fw-bold mb-3"><a href="{{ post.url | relative_url }}" class="text-dark text-decoration-none">{{ post.title }}</a></h5>
          <p class="text-muted small mb-0">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

</div>
