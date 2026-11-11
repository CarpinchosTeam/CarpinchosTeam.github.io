---
layout: base
lang: es
ref: inicio
permalink: /
title: Inicio
---

<!-- 1. HERO -->
<section class="hero-section text-center py-5 bg-primary text-white" style="background-size: cover; background-position: center; position: relative; min-height: 80vh; display: flex; align-items: center;">
  <div style="background-color: rgba(19, 50, 79, 0.85); position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></div>
  <div class="container position-relative py-5" style="z-index: 1;">
    <img src="{{ '/assets/img/logo-borderless.svg' | relative_url }}" alt="Carpinchos Logo" style="width: 300px;">
    <h1 class="display-3 fw-bolder text-white mb-4" style="letter-spacing: -1px; font-size: clamp(2.5rem, 12vw, 4.5rem) !important;">Team Carpinchos</h1>
    <h3 class="h5 fw-normal text-white mb-4" style="opacity: 0.9; letter-spacing: 1px; text-transform: uppercase;">Una iniciativa de <a href="https://supercomputo.unc.edu.ar" class="text-white fw-bold text-decoration-none border-bottom border-white pb-1">UNC Supercómputo</a></h3>
    <p class="lead fw-normal mx-auto mb-5 text-light" style="max-width: 800px; font-size: 1.5rem; line-height: 1.6;">
      Somos el equipo de Computación de Alto Rendimiento de la Universidad Nacional de Córdoba.
    </p>
    <div class="justify-content-center flex-wrap">
      <a href="#recorrido" class="btn btn-primary btn-lg px-5 m-2 shadow-lg">Conocé nuestra historia</a>
      <a href="#apoyanos" class="btn btn-outline-light btn-lg px-5 m-2">Apoyanos</a>
    </div>
  </div>
</section>

<div class="container-md mt-5">

  <!-- 2. ¿QUÉ HACEMOS? (con los números de impacto) -->
  <section class="py-5" id="que-hacemos">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">¿Qué hacemos?</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    </div>
    {% assign estudiantes = site.integrantes | where_exp: "i", "i.competitions" %}
    <div class="row mt-5">
      <div class="col-md-4 mb-5">
        <div class="pillar">
          <div class="pillar-number">{{ site.competencias | size }}</div>
          <span class="pillar-unit">competencias internacionales</span>
          <h4 class="fw-bold mb-2">Competimos</h4>
          <p class="text-muted mb-0" style="font-size: 1.1rem;">Representamos a Argentina en las competencias de supercómputo más exigentes del mundo.</p>
        </div>
      </div>
      <div class="col-md-4 mb-5">
        <div class="pillar">
          <div class="pillar-number">{{ estudiantes | size }}</div>
          <span class="pillar-unit">estudiantes</span>
          <h4 class="fw-bold mb-2">Formamos</h4>
          <p class="text-muted mb-0" style="font-size: 1.1rem;">Capacitamos a la próxima generación de profesionales y científicos en computación de alto rendimiento.</p>
        </div>
      </div>
      <div class="col-md-4 mb-5">
        <div class="pillar">
          <div class="pillar-number">{{ site.charlas | size }}</div>
          <span class="pillar-unit">charlas dictadas</span>
          <h4 class="fw-bold mb-2">Hacemos comunidad</h4>
          <p class="text-muted mb-0" style="font-size: 1.1rem;">Compartimos lo que sabemos en universidades y eventos para acercar el HPC a más personas y fortalecer el ecosistema en Argentina y Latinoamérica.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- 3. ¿POR QUÉ HACEMOS ESTO? -->
  <section class="band py-5 my-4" id="proposito">
    <div class="row justify-content-center">
      <div class="col-lg-9 text-center">
        <h2 class="display-5 fw-bold mb-4">Nuestro Propósito</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto 30px auto; border-radius: 2px;"></div>
        <p class="lead text-muted" style="font-size: 1.35rem; line-height: 1.8;">
          Las competencias de HPC son una de las formas más intensivas de formación en computación de alto rendimiento. Cada edición reúne estudiantes que durante meses aprenden optimización, programación paralela, arquitectura de computadoras y trabajo en equipo para resolver desafíos reales bajo restricciones de energía y hardware.
        </p>
        <p class="lead text-muted mt-3" style="font-size: 1.35rem; line-height: 1.8;">
          En Carpinchos usamos esas competencias como una excusa para formar profesionales y fortalecer la comunidad de HPC en Argentina.
        </p>
      </div>
    </div>
  </section>

  <!-- 5. COMPETENCIAS (Timeline) -->
  <section class="py-5 my-5" id="recorrido">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">Historia y Competencias</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
      <p class="lead text-muted mt-4">El archivo de nuestras participaciones.</p>
    </div>

    {% include timeline.html %}
  </section>

  <!-- 6. EQUIPO ACTUAL -->
  <section class="band py-5 my-5" id="equipo">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">El Equipo Actual</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    </div>

    <div class="row justify-content-center mt-5">
      {% assign active_comp = site.competencias | where: "active", true | map: "event" | first %}

      {% if active_comp %}
        <!-- Estudiantes -->
        {% for integrante in site.integrantes %}
          {% if integrante.competitions contains active_comp %}
          <div class="col-6 col-md-4 text-center mb-5">
            <a href="{{ integrante.url | relative_url }}" class="text-decoration-none">
              {% if integrante.github %}
              <img src="https://github.com/{{ integrante.github }}.png?size=150" alt="{{ integrante.name }}" class="rounded-circle mb-3 avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto; object-fit: cover;">
              {% else %}
              <div class="rounded-circle mb-3 bg-secondary d-inline-block avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto;"></div>
              {% endif %}
              <h5 class="fw-bold mb-1 text-dark">{{ integrante.name }}</h5>
              <span class="text-primary ui-font small fw-bold">{{ integrante.field }}</span>
            </a>
          </div>
          {% endif %}
        {% endfor %}
    </div>

    <!-- Coaches -->
    <div class="row justify-content-center mt-2">
        {% for integrante in site.integrantes %}
          {% if integrante.coach_competitions contains active_comp %}
          <div class="col-6 col-md-4 text-center mb-5">
            <a href="{{ integrante.url | relative_url }}" class="text-decoration-none">
              {% if integrante.github %}
              <img src="https://github.com/{{ integrante.github }}.png?size=150" alt="{{ integrante.name }}" class="rounded-circle mb-3 avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto; object-fit: cover;">
              {% else %}
              <div class="rounded-circle mb-3 bg-secondary d-inline-block avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto;"></div>
              {% endif %}
              <h5 class="fw-bold mb-1 text-dark">{{ integrante.name }} <i class="fa-solid fa-chalkboard-user text-orange ml-1"></i></h5>
              <span class="text-orange ui-font small fw-bold">Coach</span>
            </a>
          </div>
          {% endif %}
        {% endfor %}
      {% endif %}
    </div>
  </section>

  <!-- 7. SPONSORS -->
  <section class="py-5 my-5 text-center" id="sponsors">
    <h2 class="display-5 fw-bold mb-3">Nuestros Sponsors</h2>
    <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    <p class="lead text-muted mt-4 mb-5">Instituciones y empresas que apuestan por el talento universitario.</p>

    {% assign regular_sponsors = site.sponsors | where: "type", "sponsor" | sort: "order" %}
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap mt-5">
      {% for sponsor in regular_sponsors %}
      <div class="text-center">
        <a href="{{ sponsor.link }}" target="_blank" class="sponsor-logo">
          <img src="{{ 'assets/logos/' | append: sponsor.logo | relative_url }}" alt="{{ sponsor.title }}">
        </a>
        {% if sponsor.level %}
        <p class="mt-3 text-muted fw-bold small text-uppercase ui-font">{{ sponsor.level }}</p>
        {% endif %}
      </div>
      {% endfor %}
    </div>

    <h3 class="h4 fw-bold mt-5 mb-4 text-muted">Apoyo Institucional</h3>
    {% assign institutional_sponsors = site.sponsors | where: "type", "institutional" | sort: "order" %}
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap">
      {% for inst in institutional_sponsors %}
      <div class="text-center">
        <a href="{{ inst.link }}" target="_blank" class="sponsor-logo">
          <img src="{{ 'assets/logos/' | append: inst.logo | relative_url }}" alt="{{ inst.title }}">
        </a>
      </div>
      {% endfor %}
    </div>

    <div class="mt-5 pt-3">
      <a href="https://docs.google.com/presentation/d/1CdKjTrHeCHs50wEVKzI28m1R14SMBw_xwptN4yIPCAo/edit?slide=id.p#slide=id.p" target="_blank" class="btn btn-outline-primary">Convertirse en Sponsor <i class="fa-solid fa-arrow-up-right-from-square ml-2"></i></a>
    </div>
  </section>

  <!-- 8. BANCARPINCHOS -->
  <section class="my-5 bg-primary text-white rounded-lg p-4 p-md-5 shadow-lg" id="apoyanos" style="position: relative; overflow: hidden;">
    <div style="position: absolute; top: -50%; left: -10%; width: 50%; height: 200%; background: radial-gradient(closest-side, rgba(28,176,213,0.15), rgba(19,50,79,0)); pointer-events: none;"></div>
    <div class="row align-items-center position-relative" style="z-index: 1;">
      <div class="col-lg-6 mb-5 mb-lg-0 pr-lg-5">
        <h2 class="fluid-title fw-bold text-white mb-4">La comunidad que nos sostiene</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin-bottom: 30px; border-radius: 2px;"></div>
        <p class="lead mb-4" style="font-size: 1.25rem; line-height: 1.7; opacity: 0.9;">
          Más de 100 personas apoyaron económicamente al equipo.
          Además, contamos con {{ site.data.bancarpinchos | size }} personas muy especiales que aportaron más de 25 USD, convirtiéndose en nuestros <strong>Bancarpinchos</strong>.
          ¡Gracias a todos por hacer posible que representemos a la Universidad Nacional de Córdoba en competencias internacionales!
        </p>
        <div class="mt-5">
          <a href="https://cafecito.app/teamcarpinchos" target="_blank" class="btn btn-light btn-lg text-primary ui-font px-4 py-3 shadow">
            <i class="fa-solid fa-mug-hot mr-2"></i> Convertite en Bancarpincho
          </a>
        </div>
        <p class="mt-4 small ui-font" style="opacity: 0.7;">Alias ARS: teamcarpinchos &bull; Alias USD: teamcarpinchos.usd</p>
      </div>
      <div class="col-lg-6">
        <div class="bancarpinchos p-lg-4">
          <div class="bancarpinchos-header d-flex align-items-center mb-4 pb-3">
            <i class="fa-solid fa-heart text-orange fs-3 mr-2"></i>
            <h4 class="fw-bold m-0 text-white">¡Gracias Bancarpinchos!</h4>
          </div>
          <div class="bancarpinchos-list">
            <ul class="list-unstyled mb-0">
              {% for donor in site.data.bancarpinchos %}
              <li class="mb-3">
                <span class="d-block ui-font" style="font-size: 0.95rem;">{{ donor.name }}</span>
              </li>
              {% endfor %}
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 9. NOTICIAS -->
  <section class="py-5 mt-5 border-top" id="noticias" style="border-color: rgba(0,0,0,0.05) !important; border-top-width: 2px !important;">
    <div class="row align-items-center mb-5">
      <div class="col-md-8">
        <h3 class="display-6 fw-bold mb-0">Últimas Novedades</h3>
      </div>
      <div class="col-md-4 text-md-right mt-3 mt-md-0">
        <a href="{{ '/posts/' | relative_url }}" class="btn btn-outline-primary btn-sm">Ver archivo de noticias</a>
      </div>
    </div>

    <div class="row">
      {% assign posts = site.posts %}
      {% for post in posts limit:3 %}
      <div class="col-md-4 mb-4">
        <div class="card h-100 p-4">
          <div class="text-primary ui-font small fw-bold mb-3"><i class="fa-regular fa-calendar mr-2"></i>{{ post.date | date: "%d/%m/%Y" }}</div>
          <h5 class="fw-bold mb-3"><a href="{{ post.url | relative_url }}" class="text-dark text-decoration-none">{{ post.title }}</a></h5>
          <p class="text-muted small mb-0 mt-0">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

</div>
