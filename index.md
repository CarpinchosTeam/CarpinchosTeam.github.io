---
layout: home
title: Carpinchos
subtitle: This is the official website for the HPC Team
---


# Hello!

We are a Student Cluster Competition team representing the Universidad Nacional de Córdoba (UNC), Argentina.


# Competitions & Events

<div class="events-container">
{% if site.data.events %}
  {% assign sorted_events = site.data.events | sort: 'year' | reverse %}
  {% for event in sorted_events %}
    <div class="event-card">
      <h3>{{ event.year }} - {{ event.name }}</h3>
      <div class="event-details">
        <p><strong>Location:</strong> {{ event.location }}</p>
        {% if event.award %}
        <p><strong>Award:</strong> {{ event.award }}</p>
        {% endif %}
      </div>
    </div>
  {% endfor %}
{% else %}
  <p>No event data found.</p>
{% endif %}
</div>

<style>
.events-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin: 20px 0;
}
.event-card {
  background: #f8f9fa;
  border-radius: 8px;
  padding: 20px;
  width: 100%;
  max-width: 400px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.event-card h3 {
  margin-top: 0;
  color: #2c3e50;
}
.event-details {
  margin-top: 10px;
}
</style>


# Team Roster

Meet the dedicated students and mentors who make up Team Carpinchos.

{% if site.data.members %}
  {% assign status_order = "current|former" | split: "|" %} {# Define the desired order #}

  {% for status_name in status_order %}
    {% assign members_in_status = site.data.members | where: "status", status_name %}

    {% if members_in_status.size > 0 %}
<div class="roster-group">
      {% if status_name == "current" %}
<h2 class="group-header">Current Members & Coaches</h2>
      {% elsif status_name == "former" %}
<h2 class="group-header">Alumni & Former Coaches</h2>
      {% endif %}

<div style="display: flex; flex-wrap: wrap; gap: 20px;">
      {% for member in members_in_status %}
<div class="member-card">
{% if member.picture %}
<img src="{{ site.baseurl }}/{{ member.picture }}" alt="Photo of {{ member.name }}" class="member-photo">
{% else %}
<img src="https://github.com/{{ member.github }}.png?size=100" alt="GitHub profile picture of {{ member.name }}" class="member-photo">
{% endif %}
<div class="member-info">
<h4>{{ member.name }}</h4>
<p>{{ member.role }}</p>
<p>{% if member.field %}{{ member.field }}, {% endif %}{{ member.affiliation }}</p>
          {% if member.github %}
<a href="https://github.com/{{ member.github }}" target="_blank" rel="noopener noreferrer">GitHub</a>
          {% endif %}
</div>
</div>
      {% endfor %}
</div>
</div>
    {% endif %}
  {% endfor %}

{% else %}
  <p>No member data found.</p>
{% endif %}

<style>
.member-card {
  text-align: center;
  width: 250px; /* Increased width */
  padding: 15px;
  background: #f8f9fa;
  border-radius: 8px;
  transition: transform 0.2s;
}
.member-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}
.member-photo {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 10px;
}
.member-info h4 {
  margin: 5px 0;
  color: #2c3e50;
}
.member-info p {
  margin: 3px 0;
  font-size: 0.9em;
  color: #555;
}

.roster-group {
  margin-bottom: 40px;
}

.group-header {
  color: #2c3e50;
  border-bottom: 2px solid #eee;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

@media (max-width: 768px) {
  .member-card {
    width: 200px; /* Increased width for smaller screens */
  }
}
</style>