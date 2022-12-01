---
layout: post
title: "Fotos: Osaka Japão"
slug: osaka-japan
category: foto
---

<div class="image-gallery">
{% for file in site.static_files %}
  {% if file.path contains include.folder %}
    {% if file.extname == '.jpg' or 
      file.extname == '.jpeg' or 
      file.extname == '.JPG' or 
      file.extname == '.JPEG' %}

      {% assign filenameparts = file.path | split: "/" %}
      {% assign filename = filenameparts | last | replace: file.extname,"" %}

      <a href="/galeria/osaka" title="{{ filename }}">
        <img src="//images.weserv.nl/?url=jekyllcodex.org/{{ file.path }}&w=300&h=300&output=jpg&q=50&t=square" alt="{{ filename }}" />
        <span>{{ filename }}</span>
      </a>
    {% endif %}
  {% endif %}
{% endfor %}
</div>

Título #01

{% include image-gallery.html folder="/galeria/osaka" %}
