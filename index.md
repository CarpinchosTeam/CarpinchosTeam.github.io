---
layout: base
title: Inicio
---

<!-- 1. HERO -->
<section class="hero-section text-center py-5 bg-primary text-white" style="background-image: url('{{ '/assets/img/hero-placeholder.jpg' | relative_url }}'); background-size: cover; background-position: center; position: relative;">
  <div style="background-color: rgba(3, 0, 42, 0.85); position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></div>
  <div class="container position-relative py-5" style="z-index: 1;">
    <img src="{{ '/assets/img/logo-carpincho.svg' | relative_url }}" alt="Carpinchos Logo" style="width: 200px; margin-bottom: 2rem;">
    <h1 class="display-4 fw-bolder text-white">Equipo Carpinchos</h1>
    <p class="lead fw-normal mx-auto mb-5 text-light" style="max-width: 800px; font-size: 1.5rem;">
      Somos el equipo de Computación de Alto Rendimiento de la Universidad Nacional de Córdoba.
    </p>
    <div class="d-flex justify-content-center gap-3">
      <a href="#recorrido" class="btn btn-primary btn-lg px-4">Conocé nuestra historia</a>
      <a href="#apoyanos" class="btn btn-outline-light btn-lg px-4">Apoyanos</a>
    </div>
  </div>
</section>

<div class="container-md mt-5">

  <!-- 2. ¿QUÉ HACEMOS? -->
  <section class="py-5" id="que-hacemos">
    <h2 class="text-center mb-5">¿Qué hacemos?</h2>
    <div class="row text-center">
      <div class="col-md-4 mb-4">
        <h1 class="text-primary mb-3">🏆</h1>
        <h4 class="fw-bold">Competimos internacionalmente</h4>
        <p class="text-muted">Representamos a Argentina en las competencias de supercómputo más exigentes del mundo.</p>
      </div>
      <div class="col-md-4 mb-4">
        <h1 class="text-primary mb-3">📚</h1>
        <h4 class="fw-bold">Formamos estudiantes</h4>
        <p class="text-muted">Capacitamos a la próxima generación de profesionales y científicos en computación de alto rendimiento.</p>
      </div>
      <div class="col-md-4 mb-4">
        <h1 class="text-primary mb-3">💻</h1>
        <h4 class="fw-bold">Desarrollamos tecnología</h4>
        <p class="text-muted">Creamos software, optimizamos algoritmos y diseñamos infraestructura para resolver problemas complejos.</p>
      </div>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 3. ¿POR QUÉ HACEMOS ESTO? -->
  <section class="py-5" id="proposito">
    <div class="row justify-content-center">
      <div class="col-lg-8 text-center">
        <h2 class="mb-4">¿Por qué hacemos esto?</h2>
        <p class="lead text-muted">
          Las competencias internacionales no son un fin en sí mismo, sino una poderosa herramienta. Las utilizamos como motor para <strong>formar estudiantes de excelencia en HPC</strong>, desarrollar tecnologías de vanguardia y fortalecer la comunidad científica y tecnológica de nuestra región.
        </p>
      </div>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 4. IMPACTO -->
  <section class="py-5 bg-light rounded-4 p-5 text-center" id="impacto">
    <h2 class="mb-5">Nuestro Impacto</h2>
    <div class="row">
      <div class="col-6 col-md-3 mb-4">
        <h2 class="display-4 fw-bold text-primary">{{ site.competencias | size }}</h2>
        <p class="text-uppercase fw-bold text-muted small">Competencias Internacionales</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <h2 class="display-4 fw-bold text-primary">{{ site.integrantes | size }}</h2>
        <p class="text-uppercase fw-bold text-muted small">Estudiantes Formados</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <h2 class="display-4 fw-bold text-primary">50+</h2>
        <p class="text-uppercase fw-bold text-muted small">Bancarpinchos Activos</p>
      </div>
      <div class="col-6 col-md-3 mb-4">
        <h2 class="display-4 fw-bold text-primary">3</h2>
        <p class="text-uppercase fw-bold text-muted small">Sponsors Institucionales</p>
      </div>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 5. COMPETENCIAS -->
  <section class="py-5" id="recorrido">
    <h2 class="text-center mb-5">Competencias Destacadas</h2>
    
    <div class="row">
      {% for comp in site.competencias reversed limit:4 %}
      <div class="col-md-6 mb-4">
        <div class="card h-100 border-0 bg-light p-4 shadow-sm">
          <h4 class="fw-bold"><a href="{{ comp.url | relative_url }}" class="text-decoration-none text-dark">{{ comp.name }}</a></h4>
          <p class="text-primary fw-bold mb-2">{{ comp.year }} &bull; {{ comp.location }}</p>
          {% if comp.award %}
          <p class="mb-0 mt-3">🏆 <strong>Premio:</strong> {{ comp.award }}</p>
          {% endif %}
          <div class="mt-3">
            <a href="{{ comp.url | relative_url }}" class="fw-bold text-primary">Ver todos los detalles y resultados &rarr;</a>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>

    <div class="text-center mt-4">
      <a href="{{ '/competencias' | relative_url }}" class="btn btn-outline-primary">Ver archivo histórico completo</a>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 6. EQUIPO ACTUAL -->
  <section class="py-5" id="equipo">
    <h2 class="text-center mb-5">El Equipo Actual</h2>
    <div class="row justify-content-center">
      {% assign current_members = site.integrantes | where: "status", 'current' %}
      {% for integrante in current_members %}
      <div class="col-6 col-md-4 col-lg-3 text-center mb-4">
        {% if integrante.github %}
        <img src="https://github.com/{{ integrante.github }}.png?size=150" alt="{{ integrante.name }}" class="rounded-circle mb-3 shadow-sm" style="width: 120px; height: 120px; object-fit: cover;">
        {% else %}
        <div class="rounded-circle mb-3 bg-secondary d-inline-block shadow-sm" style="width: 120px; height: 120px;"></div>
        {% endif %}
        <h5 class="fw-bold mb-1"><a href="{{ integrante.url | relative_url }}" class="text-decoration-none text-dark">{{ integrante.name }}</a></h5>
        <p class="text-muted small">{{ integrante.role }}</p>
      </div>
      {% endfor %}
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 7. SPONSORS -->
  <section class="py-5 text-center" id="sponsors">
    <h2 class="mb-5">Nuestros Sponsors</h2>
    <p class="lead text-muted mb-5">Instituciones y empresas que apuestan por el talento universitario.</p>
    
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap">
      <div>
        <a href="https://inpunto.la/" target="_blank" class="text-decoration-none text-dark">
          <div class="bg-light rounded p-4 shadow-sm" style="width: 200px; height: 100px; display: flex; align-items: center; justify-content: center;">
            <h4 class="m-0 fw-bold">InPunto</h4>
          </div>
        </a>
        <p class="mt-2 text-muted fw-bold small">Sponsor Oro</p>
      </div>
      <div>
        <a href="https://txpipe.io/" target="_blank" class="text-decoration-none text-dark">
          <div class="bg-light rounded p-4 shadow-sm" style="width: 200px; height: 100px; display: flex; align-items: center; justify-content: center;">
            <h4 class="m-0 fw-bold">TxPipe</h4>
          </div>
        </a>
        <p class="mt-2 text-muted fw-bold small">Sponsor Plata</p>
      </div>
      <div>
        <a href="https://nerdearla.com/" target="_blank" class="text-decoration-none text-dark">
          <div class="bg-light rounded p-4 shadow-sm" style="width: 200px; height: 100px; display: flex; align-items: center; justify-content: center;">
            <h4 class="m-0 fw-bold">Nerdearla</h4>
          </div>
        </a>
        <p class="mt-2 text-muted fw-bold small">Sponsor Bronce</p>
      </div>
    </div>

    <div class="mt-5">
      <a href="https://docs.google.com/presentation/d/1CdKjTrHeCHs50wEVKzI28m1R14SMBw_xwptN4yIPCAo/edit?slide=id.p#slide=id.p" target="_blank" class="btn btn-outline-primary">Sumate a los sponsors (Carta de Intención)</a>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 8. BANCARPINCHOS -->
  <section class="py-5 bg-primary text-white rounded-4 p-5" id="apoyanos">
    <div class="row align-items-center">
      <div class="col-lg-6 mb-4 mb-lg-0">
        <h2 class="text-white mb-4">La comunidad que nos sostiene</h2>
        <p class="lead">
          Más de 50 personas apoyan económicamente al equipo y hacen posible que representemos a la Universidad Nacional de Córdoba en competencias internacionales. A ellos los llamamos <strong>Bancarpinchos</strong>.
        </p>
        <div class="d-flex gap-3 mt-4">
          <a href="https://cafecito.app/teamcarpinchos" target="_blank" class="btn btn-light btn-lg text-primary fw-bold">☕ Convertite en Bancarpincho</a>
        </div>
        <p class="mt-3 small opacity-75">Alias ARS: teamcarpinchos &bull; Alias USD: teamcarpinchos.usd</p>
      </div>
      <div class="col-lg-6">
        <div class="bg-white text-dark rounded p-4 shadow" style="max-height: 300px; overflow-y: auto;">
          <h5 class="fw-bold mb-3 border-bottom pb-2">¡Gracias Bancarpinchos!</h5>
          <ul class="list-unstyled mb-0" style="column-count: 2;">
            <li class="mb-2">Hormann Manrique Nicolas</li>
            <li class="mb-2">Zapico Barrionuevo</li>
            <li class="mb-2">Alejandro Peralta Frias</li>
            <li class="mb-2">Hernan Enrique Modrow</li>
            <li class="mb-2">Rocio Diaz Martin</li>
            <li class="mb-2">Diego Piloni</li>
            <li class="mb-2">Adrian Marcelo Edelste</li>
            <li class="mb-2">TxPipe</li>
            <li class="mb-2">Alejandro Peralta Frias (Ale)</li>
            <li class="mb-2">Juana Salas</li>
            <li class="mb-2">Eric Gabriel Hegi</li>
            <li class="mb-2">Fran</li>
            <li class="mb-2">Francisco Matias Cuenca</li>
            <li class="mb-2">Feraud Santiago</li>
            <li class="mb-2">Paz Roberto Jose Roque</li>
            <li class="mb-2">Jorge Carlos Gabriel F</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <hr class="my-5 opacity-25">

  <!-- 9. NOTICIAS -->
  <section class="py-5" id="noticias">
    <h3 class="mb-4">Últimas Noticias</h3>
    <ul class="list-unstyled">
      {% assign posts = site.posts %}
      {% for post in posts limit:3 %}
      <li class="mb-3">
        <span class="text-muted small me-3">{{ post.date | date: "%d/%m/%Y" }}</span>
        <a href="{{ post.url | relative_url }}" class="fw-bold text-dark text-decoration-none">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
    <div class="mt-3">
      <a href="{{ '/tags' | relative_url }}" class="fw-bold text-primary">Ver todas las noticias &rarr;</a>
    </div>
  </section>

</div>
