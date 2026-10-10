---
layout: page
title: Projets
permalink: /projets/
---

<style>
  /* Cache complètement le grand titre de la page */
  h1, .post-title, .page-heading {
    display: none;
  }
</style>

<style>
  /* Centre le grand titre de la page */
  h1, .post-title, .page-heading {
    text-align: center;
    margin-bottom: 30px; /* Ajoute un peu d'espace sous le titre */
  }
</style>

<div class="stage-list">
{% assign year = nil %}
{% for post in site.categories.projet %}
  
  <!-- Gestion des années -->
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <h2 style="margin-top: 30px; margin-bottom: 15px; border-bottom: 1px solid #eee; padding-bottom: 5px; color: #333; font-size: 0.7em;">{{ y }}</h2>
  {% endif %}
  
  <!-- Bloc principal du stage  -->
  <div style="display: flex; align-items: stretch; margin-bottom: 15px;">
    
    {% if post.image %}
    <div style="flex: 0 0 30%; max-width: 250px; margin-right: 15px; display: flex; align-items: center; justify-content: center;">
      <a href="{{ post.url | prepend: site.baseurl }}" style="width: 100%;">
        <img src="{{ site.baseurl }}{{ post.image }}" style="width: 100%; height: 200px; object-fit: contain; display: block;">
      </a>
    </div>
    {% endif %}

    <!-- Colonne Texte (boîte fine) -->
    <div style="flex: 1; background-color: #f4f4f9; border-left: 3px solid #2215d7; padding: 10px 15px; display: flex; flex-direction: column; justify-content: center;">
      
      <a href="{{ post.url | prepend: site.baseurl }}" style="text-decoration: none;">
        <h3 style="margin-top: 0; margin-bottom: 5px; color: #1e00ff; font-weight: bold; font-size: 1em;">
          {{ post.title }}
        </h3>
      </a>
      
      <p style="margin: 0; color: #333; line-height: 1.4; font-size: 0.85em;">
        {% if post.description %}
          {{ post.description }}
        {% else %}
          {{ post.excerpt | strip_html | truncatewords: 25 }}
        {% endif %}
      </p>

    </div>

  </div>
{% endfor %}
</div>