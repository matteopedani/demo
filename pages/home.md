---
layout: default
title: "demo.pedani.it"
permalink: "/home"
description: "un sito per le demo"
background: "/img/bg-post.jpg"
form: true
tipo: "prima pagina"
---

  <header>

  <div id="carouselExampleIndicators" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
        <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
      </ol>
  <div class="carousel-inner" role="listbox">


  <div class="carousel-item active" style="background-image: url('/images/arance.jpg')">
          <div class="carousel-caption d-none d-md-block">
            <h1>{{site.title}}</h1>
            <h6>
            {{site.description}}
            </h6>
          </div>
        </div>

{% for primapagina in site.pages %}
{% if primapagina.type == 'primapagina' %}
{% if primapagina.slide  %}
   <div class="carousel-item " style="background-image: url('{{primapagina.slide}}')">
          <div class="carousel-caption d-none d-md-block">
            <h1>{{primapagina.title}}</h1>
            <h6>{{ primapagina.description }}</h6>
          </div>
        </div>
{{primapagina.title}}
{% endif %}
{% endif %}
{% endfor %}



<div class="carousel-item" style="background-image: url('/images/IMG_9085_elab_testata.jpg')">
      <div class="carousel-caption d-none d-md-block">
      <h3>Third Slide</h3>
            <p>This is a description for the third slide.</p>
          </div>
</div>



  </div>

  <a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">{{site.lang.previus}}</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">{{site.lang.next}}</span>
      </a>
    </div>
  </header>




  <!-- Page Content -->
  <div class="container">


   <!-- Features Section -->

   <div class="row">
      <div class="col-lg-6">
        <h2>Tempora minima</h2>
        <p>Peiciendis quia dolorum ducimus unde.</p>
        <ul>
          <li>
            <strong>Aspernatur tempora</strong>
          </li>
          <li>Quisquam</li>
          <li>Lorem ipsum dolor sit amet.</li>
          <li>Corporis, omnis doloremque non cum.</li>
          <li>Aspernatur tempora minima unde aliquid ea culpa sunt.</li>
        </ul>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Corporis, omnis doloremque non cum id reprehenderit, quisquam totam aspernatur tempora minima unde aliquid ea culpa sunt. Reiciendis quia dolorum ducimus unde.</p>
      </div>
      <div class="col-lg-6">
        <img class="img-fluid rounded" src="/images/riso_curcuma.jpg" alt="">
      </div>
    </div>

<br>

<div class="row">
{% for primapagina in site.pages %}
{% if primapagina.type == 'primapagina' %}

<div class="col-lg-4 col-sm-6 portfolio-item">
  <div class="card h-100">
    <a href="{{primapagina.url}}"><img class="card-img-top" src="{{primapagina.image}}" alt=""></a>
    <div class="card-body">
    <h4 class="card-title">
      <a href="{{primapagina.url}}">
        {{primapagina.title}}
      </a>
    </h4>
    <h6 class="card-text">
      {{ primapagina.description }}
    </h6>
    </div>
  </div>
</div>
{% endif %}
{% endfor %}


  </div>



   <hr>
   <div class="row mb-4">
      <div class="col-md-8">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Molestias, expedita, saepe, vero rerum deleniti beatae veniam harum neque nemo praesentium cum alias asperiores commodi.</p>
      </div>
      <div class="col-md-4">
        <a class="btn btn-lg btn-secondary btn-block" href="/ristorante/">Prenota</a>
      </div>
    </div>

<!-- 

{% for post in site.posts  %}
  {% if post.tipo == page.tipo %}
<article class="post-preview">

  <a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">
    <h2 class="post-title">{{ post.title }}</h2>
    {% if post.subtitle %}
    <h3 class="post-subtitle">{{ post.subtitle }}</h3>
    {% else %}
    <h3 class="post-subtitle">{{ post.excerpt | strip_html | truncatewords: 15 }}</h3>
    {% endif %}
  </a>
  <p class="post-meta">
   {% include date.html  date=post.date %} 
  </p>

</article>
  </div>
-->
  <!-- /.container -->


<hr>
    {% endif %}

{% endfor %}
