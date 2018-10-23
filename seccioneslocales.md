---
layout: page
title: Secciones Locales
permalink: /seccioneslocales/
redirect_from:
---

{% assign n = 0 %}
{% for item in site.data.LC %}
	{% assign n = n | plus: 1 %}
{% endfor %}

EstudiantesRSEF cuenta por el momento con {{ n }} Secciones Locales en:

<ul class="collection">
	{% for item in site.data.LCR %}
	  <li class="collection-item avatar" id="{{ item.nome }}">
	    <img src="{{ item.img }}" alt="" class="circle">
	    <span class="title">
				Sección Local de {{ item.nome }}
			</span>
	    <p>
				Presidente: {{ item.presidente }}
				<br>
	      	Fundador: {{ item.fondazione }}
				<br>
				{% if item.ex != nil %}
					Ex-Presidente: {{ item.ex }}
				{% endif %} 				
	    </p>
	    <div class="secondary-content">
				{% if item.fb != nil %}
					<a href="{{ item.fb }}" title="Página de Facebook">
						<i class="fa fa-lg fa-facebook-square" aria-hidden="true"></i>
					</a>
				{% endif %}
				{% if item.regolamento != nil %}
		      <a href="{{ item.regolamento }}" title="Reglamento Interno">
						<i class="fa fa-lg fa-file-text"></i>
					</a>
				{% endif %}
	      <a href="mailto:{{ item.mail }}&#64;&#97;&#105;&#45;&#115;&#102;&#46;&#105;&#116;" title="Dirección electrónica">
					<i class="fa fa-lg fa-envelope"></i>
				</a>
			</div>
	  </li>
	{% endfor %}
</ul>


## ¿Quieres crear una nueva Sección Local?

Consulta [esta](/nuevaseccionlocal/) página.
