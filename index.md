---
layout: home
title: Carpinchos
subtitle: This is the official website for the HPC Team
---


We are a Student Cluster Competition team representing the Universidad Nacional de Córdoba (UNC), Argentina.


# Competitions & Events

{% include timeline.html %}

# Team Roster

Meet the dedicated students and mentors who make up Team Carpinchos.

## Current Members & Coaches

{% assign members = site.data.members | where: "status", 'current' %}
{% include members.html %}

## Alumni & Former Coaches

{% assign members = site.data.members | where: "status", 'former' %}
{% include members.html %}

# Posts
