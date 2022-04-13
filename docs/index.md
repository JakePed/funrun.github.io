---
layout: home
title: Home
exclude: true
---
<img src="https://bafybeifmsiihs3gb5hx6vddfkgpk2wlpvuq424stzyy4ybrrod4lwb7hde.ipfs.dweb.link/" max-width="100%" height="auto">
<style>
h1 {text-align: center;}
  </style>
  <h1>A creative collection cellebrating bitcoin</h1>

<ul class="assets">
{% for series in site.series %}

  <li>
    <img src="{% if series.image != null and series.image != '' %}{{ series.image }}{% else %}{{'assets/placeholder.png' | relative_url}}{% endif %}">
    <a href="/{{ series.name | downcase }}">
         <b>{{ series.name }}</b>
    </a>    
  </li>
{% endfor %}
</ul>
