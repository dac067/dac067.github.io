---
layout: default
title: Etc
permalink: /etc/
order: 3
---

<div class="portfolio">

  <h1 class="page-heading">Etc</h1>

  <div class="post-gallery">
    {% assign loopindex = 0 %}
    {% for post in site.categories.etc %}
    {% assign loopindex = loopindex | plus: 1 %}
    {% assign rowfinder = loopindex | modulo: 3 %}
    {% if rowfinder == 1 %}
        <div class="col-4">
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
            <img class="post-thumbnail" src="{{ site.url}}/assets/{{ post.thumbnail }}" alt= "{{ post.thumbnail }}" >
          </a>
        </div>

    {% elsif rowfinder == 0 %}

        <div class="col-4">
          <h2>
            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
          </h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
            <img class="post-thumbnail" src="{{ site.url}}/assets/{{ post.thumbnail }}" alt= "{{ post.thumbnail }}" >
          </a>
        </div>


  {% else %}

      <div class="col-4">
        <h2>
          <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        </h2>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
          <img class="post-thumbnail" src="{{ site.url}}/assets/{{ post.thumbnail }}" alt= "{{ post.thumbnail }}" >
        </a>
      </div>

    {% endif %}
{% endfor %}
{% if rowfinder != 0 %}
      </div>
{% endif %}
