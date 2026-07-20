---
layout: base
lang: en
ref: inicio
permalink: /en/
title: Inicio
---

<!-- 1. HERO -->
<section class="hero-section text-center py-5 bg-primary text-white" style="background-size: cover; background-position: center; position: relative; min-height: 80vh; display: flex; align-items: center;">
  <div style="background-color: rgba(3, 0, 42, 0.85); position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></div>
  <div class="container position-relative py-5" style="z-index: 1;">
    <img src="{{ '/assets/img/logo-carpincho.svg' | relative_url }}" alt="Carpinchos Logo" style="width: 220px; margin-bottom: 2.5rem; filter: drop-shadow(0 4px 6px rgba(0,0,0,0.3));">
    <h1 class="display-3 fw-bolder text-white mb-4" style="letter-spacing: -1px; font-size: clamp(2.5rem, 12vw, 4.5rem) !important;">Team Carpinchos</h1>
    <h3 class="h5 fw-normal text-white mb-4" style="opacity: 0.9; letter-spacing: 1px; text-transform: uppercase;">An initiative by <a href="https://supercomputo.unc.edu.ar" class="text-white fw-bold text-decoration-none border-bottom border-white pb-1">UNC Supercómputo</a></h3>
    <p class="lead fw-normal mx-auto mb-5 text-light" style="max-width: 800px; font-size: 1.5rem; line-height: 1.6;">
      We are the High-Performance Computing team from the National University of Córdoba.
    </p>
    <div class="justify-content-center flex-wrap">
      <a href="#recorrido" class="btn btn-primary btn-lg px-5 m-2 shadow-lg">Our Story</a>
      <a href="#apoyanos" class="btn btn-outline-light btn-lg px-5 m-2">Support us</a>
    </div>
  </div>
</section>

<div class="container-md mt-5">

  <!-- 2. ¿QUÉ HACEMOS? -->
  <section class="py-5" id="que-hacemos">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">What do we do?</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    </div>
    <div class="row text-center mt-5">
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-orange">
          <i class="fa-solid fa-trophy" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">We compete internationally</h4>
        <p class="text-muted" style="font-size: 1.1rem;">We represent Argentina in the most demanding supercomputing competitions in the world.</p>
      </div>
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-orange">
          <i class="fa-solid fa-graduation-cap" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">We form students</h4>
        <p class="text-muted" style="font-size: 1.1rem;">We prepare the next generation of professionals and scientists in high-performance computing.</p>
      </div>
      <div class="col-md-4 mb-5 px-4">
        <div class="mb-4 text-orange">
          <i class="fa-solid fa-users" style="font-size: 4rem;"></i>
        </div>
        <h4 class="fw-bold mb-3">We strengthen the HPC ecosystem</h4>
        <p class="text-muted" style="font-size: 1.1rem;">We share knowledge and collaborate with the community to drive HPC in Argentina and the region.</p>
      </div>
    </div>
  </section>

  <!-- 3. ¿POR QUÉ HACEMOS ESTO? -->
  <section class="py-5 my-4" id="proposito">
    <div class="row justify-content-center">
      <div class="col-lg-9 text-center">
        <h2 class="display-5 fw-bold mb-4">Our Purpose</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto 30px auto; border-radius: 2px;"></div>
        <p class="lead text-muted" style="font-size: 1.35rem; line-height: 1.8;">
          HPC competitions are one of the most intensive forms of training in high-performance computing. Each edition brings together students who, for months, learn optimization, parallel programming, computer architecture, and teamwork to solve real-world challenges under power and hardware constraints.
        </p>
        <p class="lead text-muted mt-3" style="font-size: 1.35rem; line-height: 1.8;">
          At Carpinchos, we use these competitions as an an excuse to train professionals and strengthen the HPC community in Argentina.
        </p>
      </div>
    </div>
  </section>

  <!-- 4. IMPACTO -->
  <section class="bg-white rounded-lg p-2 py-4 text-center shadow-sm my-5" id="impacto">
    <h2 class="display-5 fw-bold mb-3">The Impact</h2>
    <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto 30px auto; border-radius: 2px;"></div>
    <div class="row mt-4">
      <div class="col-6 col-md-3">
        <div class="impact-number">{{ site.competencias | size }}</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px; font-size: clamp(0.65rem, 3.5vw, 0.875rem); word-break: break-word;">International<br>Competitions</p>
      </div>
      <div class="col-6 col-md-3">
        <div class="impact-number">{{ site.integrantes | size }}</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px; font-size: clamp(0.65rem, 3.5vw, 0.875rem); word-break: break-word;">Formed<br>Students</p>
      </div>
      <div class="col-6 col-md-3">
        <div class="impact-number">+100</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px; font-size: clamp(0.65rem, 3.5vw, 0.875rem); word-break: break-word;">Capybackers</p>
      </div>
      <div class="col-6 col-md-3">
        <div class="impact-number">5</div>
        <p class="text-uppercase fw-bold text-muted small ui-font" style="letter-spacing: 1px; font-size: clamp(0.65rem, 3.5vw, 0.875rem); word-break: break-word;">Sponsors &<br>Institutions</p>
      </div>
    </div>
  </section>

  <!-- 5. COMPETENCIAS (Timeline) -->
  <section class="py-5 my-5" id="recorrido">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">Story and Competitions</h2>
      <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
      <p class="lead text-muted mt-4">An archive of our journey</p>
    </div>
    
    <div class="timeline mt-5">
      {% assign comps_sorted = site.competencias | sort: "year" | reverse %}
      {% for comp in comps_sorted %}
      <div class="timeline-item">
        <div class="timeline-content">
          <div class="timeline-year">{{ comp.year }}</div>
          <h4 class="fw-bold mb-2 mt-1"><a href="{{ comp.url | relative_url }}" class="text-decoration-none text-dark">{{ comp.name }}</a></h4>
          <span class="text-muted mb-2"><i class="fa-solid fa-location-dot mr-2 text-primary"></i>{{ comp.location }}</span>
          {% if comp.awards %}
            {% for award in comp.awards %}
            <br>
            <span class="text-orange fw-bold small ui-font {% if forloop.last == false %}mb-1{% endif %}">
            <i class="fa-solid fa-award mr-2"></i>
            {{ award }}
            </span>
            {% endfor %}
          {% endif %}
          <div>
            <a href="{{ comp.url | relative_url }}" class="fw-bold text-primary ui-font text-decoration-none" style="font-size: 0.9rem;">More details <i class="fa-solid fa-arrow-right ml-1"></i></a>
          </div>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

  <!-- 6. EQUIPO ACTUAL -->
  <section class="py-5 my-5 bg-white rounded-lg p-5 shadow-sm" id="equipo">
    <div class="text-center mb-5">
      <h2 class="display-5 fw-bold mb-3">The Current Team</h2>
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
              <img src="https://github.com/{{ integrante.github }}.png?size=150" alt="{{ integrante.name }}" class="rounded-circle mb-3 avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto; object-fit: cover; border-color: var(--accent-orange);">
              {% else %}
              <div class="rounded-circle mb-3 bg-secondary d-inline-block avatar-circle" style="width: 130px; max-width: 100%; aspect-ratio: 1/1; height: auto; border-color: var(--accent-orange);"></div>
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
    <h2 class="display-5 fw-bold mb-3">Our Sponsors</h2>
    <div style="width: 60px; height: 4px; background-color: var(--accent); margin: 0 auto; border-radius: 2px;"></div>
    <p class="lead text-muted mt-4 mb-5">Institutions and companies supporting university talent.</p>
    
    {% assign regular_sponsors = site.sponsors | where: "type", "sponsor" | sort: "order" %}
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap mt-5">
      {% for sponsor in regular_sponsors %}
      <div class="text-center">
        <a href="{{ sponsor.link }}" target="_blank" class="text-decoration-none text-dark d-block card bg-transparent p-4" style="width: 220px; height: 120px; display: flex !important; align-items: center; justify-content: center;">
          <img src="{{ 'assets/logos/' | append: sponsor.logo | relative_url }}" alt="{{ sponsor.title }}" class="img-fluid" style="max-height: 80px; max-width: 100%; object-fit: contain;">
        </a>
        {% if sponsor.level %}
        <p class="mt-3 text-muted fw-bold small text-uppercase ui-font">{{ sponsor.level }}</p>
        {% endif %}
      </div>
      {% endfor %}
    </div>

    <h3 class="h4 fw-bold mt-5 mb-4 text-muted">Institutional Support</h3>
    {% assign institutional_sponsors = site.sponsors | where: "type", "institutional" | sort: "order" %}
    <div class="d-flex justify-content-center align-items-center gap-5 flex-wrap">
      {% for inst in institutional_sponsors %}
      <div class="text-center">
        <a href="{{ inst.link }}" target="_blank" class="text-decoration-none text-dark d-block card bg-transparent p-4" style="width: 220px; height: 120px; display: flex !important; align-items: center; justify-content: center;">
          <img src="{{ 'assets/logos/' | append: inst.logo | relative_url }}" alt="{{ inst.title }}" class="img-fluid" style="max-height: 80px; max-width: 100%; object-fit: contain;">
        </a>
      </div>
      {% endfor %}
    </div>

    <div class="mt-5 pt-3">
      <a href="https://docs.google.com/presentation/d/1CdKjTrHeCHs50wEVKzI28m1R14SMBw_xwptN4yIPCAo/edit?slide=id.p#slide=id.p" target="_blank" class="btn btn-outline-primary">Become a Sponsor <i class="fa-solid fa-arrow-up-right-from-square ml-2"></i></a>
    </div>
  </section>

  <!-- 8. BANCARPINCHOS -->
  <section class="py-5 my-5 bg-primary text-white rounded-lg p-5 shadow-lg" id="apoyanos" style="position: relative; overflow: hidden;">
    <div style="position: absolute; top: -50%; left: -10%; width: 50%; height: 200%; background: radial-gradient(circle, rgba(5,160,175,0.15) 0%, rgba(3,0,42,0) 70%); pointer-events: none;"></div>
    <div class="row align-items-center position-relative" style="z-index: 1;">
      <div class="col-lg-6 mb-5 mb-lg-0 pr-lg-5">
        <h2 class="display-4 fw-bold text-white mb-4">The community behind us</h2>
        <div style="width: 60px; height: 4px; background-color: var(--accent); margin-bottom: 30px; border-radius: 2px;"></div>
        <p class="lead mb-4" style="font-size: 1.25rem; line-height: 1.7; opacity: 0.9;">
          Over 100 people supported the team financially.
          Plus, we had {{ site.data.bancarpinchos | size }} very special individuals contribute over $25 USD, becoming our official <strong>CapyBackers</strong>.
          Thank you all for making it possible for us to represent the National University of Córdoba in international competitions!
        </p>
        <div class="mt-5">
          <a href="https://cafecito.app/teamcarpinchos" target="_blank" class="btn btn-light btn-lg text-primary ui-font px-4 py-3 shadow">
            <i class="fa-solid fa-mug-hot mr-2"></i> Become a CapyBacker
          </a>
        </div>
        <p class="mt-4 small ui-font" style="opacity: 0.7;">Alias ARS: teamcarpinchos &bull; Alias USD: teamcarpinchos.usd</p>
      </div>
      <div class="col-lg-6">
        <div class="bg-white text-dark rounded-lg p-4 p-md-5 shadow-lg">
          <div class="d-flex align-items-center mb-4 border-bottom pb-3">
            <i class="fa-solid fa-heart text-orange fs-3 mr-2"></i>
            <h4 class="fw-bold m-0">Thanks CapyBackers!</h4>
          </div>
          <div class="bancarpinchos-list pr-3" style="max-height: 350px; overflow-y: auto;">
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
  <section class="py-5 mt-5 border-top" id="noticias" style="border-color: rgba(0,0,0,0.05) !important; border-top-width: 2px !important;">
    <div class="row align-items-center mb-5">
      <div class="col-md-8">
        <h3 class="display-6 fw-bold mb-0">What's New</h3>
      </div>
      <div class="col-md-4 text-md-right mt-3 mt-md-0">
        <a href="{{ '/posts/' | relative_url }}" class="btn btn-outline-primary btn-sm">See all news</a>
      </div>
    </div>
    
    <div class="row">
      {% assign posts = site.posts %}
      {% for post in posts limit:3 %}
      <div class="col-md-4 mb-4">
        <div class="card h-100 bg-white p-4">
          <div class="text-primary ui-font small fw-bold mb-3"><i class="fa-regular fa-calendar mr-2"></i>{{ post.date | date: "%d/%m/%Y" }}</div>
          <h5 class="fw-bold mb-3"><a href="{{ post.url | relative_url }}" class="text-dark text-decoration-none">{{ post.title }}</a></h5>
          <p class="text-muted small mb-0 mt-0">{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
        </div>
      </div>
      {% endfor %}
    </div>
  </section>

</div>
