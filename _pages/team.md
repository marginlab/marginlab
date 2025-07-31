---
title: "MARGIN Lab - Team"
layout: gridlay
excerpt: "Allan Lab: Team members"
sitemap: false
permalink: /team/
---

## <span style="color: #8C1D40;"><strong>PI</strong></span>
{% assign number_printed = 0 %}
{% for member in site.data.pi %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left" />
  <h4 style="font-size: 2.4rem; font-weight: 600; margin-top: 32px; margin-bottom: 0.25rem;">
    {{ member.name }}
  </h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <!-- <ul style="overflow: hidden"> -->

  {% if member.number_educ >= 1 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education1 }}</p>
{% endif %}
{% if member.number_educ >= 2 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education2 }}</p>
{% endif %}
{% if member.number_educ >= 3 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education3 }}</p>
{% endif %}
{% if member.number_educ >= 4 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education4 }}</p>
{% endif %}
{% if member.number_educ == 5 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education5 }}</p>
{% endif %}

  <div style="margin-bottom: 2rem;"></div>

  <p style="margin-top: 1rem; font-size: 0.95em; white-space: nowrap;">
  <a href="mailto:{{ member.email }}">{{ member.email }}</a> |
  <a href="{{ member.website }}" target="_blank">Personal Website</a> |
  <a href="{{ member.google_scholar }}" target="_blank">Google Scholar</a>
</p>


  <!-- </ul> -->
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## <span style="color: #8C1D40;"><strong>PhDs</strong></span>
{% assign number_printed = 0 %}
{% for member in site.data.phds %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <!--<img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left" />-->
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left; margin-right: 20px; margin-bottom: 10px;" />

  <div style="overflow: hidden;">
    <!--<h4 style="font-size: 2.4rem; font-weight: 600; margin-top: 32px; margin-bottom: 0.25rem;">-->
    <h4 style="font-size: 2.4rem; font-weight: 600; margin-top: 0; margin-bottom: 0.25rem;">
      {{ member.name }}
    </h4>
    <!--<i>{{ member.info }}-->
    <i>{{ member.info }}</i> <!--<br>email: <{{ member.email }}></i> -->
  <!-- <ul style="overflow: hidden"> -->
    {% if member.number_educ >= 1 %}
      <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education1 }}</p>
    {% endif %}
    {% if member.number_educ >= 2 %}
      <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education2 }}</p>
    {% endif %}
    {% if member.number_educ >= 3 %}
      <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education3 }}</p>
    {% endif %}
    {% if member.number_educ >= 4 %}
      <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education4 }}</p>
    {% endif %}
    {% if member.number_educ == 5 %}
      <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education5 }}</p>
    {% endif %}
    {% if member.email or member.website or member.google_scholar %}
      <p style="margin-top: 1rem; font-size: 0.95em; white-space: nowrap;">
        {% assign link_parts = "" %}
        {% if member.email %}
          {% assign link_parts = link_parts | append: '<a href="mailto:' | append: member.email | append: '">' | append: member.email | append: '</a>' %}
        {% endif %}
        {% if member.website %}
          {% if link_parts != "" %}
            {% assign link_parts = link_parts | append: ' | ' %}
          {% endif %}
          {% assign link_parts = link_parts | append: '<a href="' | append: member.website | append: '" target="_blank">Personal Website</a>' %}
        {% endif %}
        {% if member.google_scholar %}
          {% if link_parts != "" %}
            {% assign link_parts = link_parts | append: ' | ' %}
          {% endif %}
          {% assign link_parts = link_parts | append: '<a href="' | append: member.google_scholar | append: '" target="_blank">Google Scholar</a>' %}
        {% endif %}
        {{ link_parts | raw }}
      </p>
    {% endif %}
  </div>
  <!-- </ul> -->
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## <span style="color: #8C1D40;"><strong>Master and Bachelor Students</strong></span>
{% assign number_printed = 0 %}
{% for member in site.data.ms_and_undergrad %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="20%" style="float: left" />
  <h4 style="font-size: 2.4rem; font-weight: 600; margin-top: 32px; margin-bottom: 0.25rem;">
    {{ member.name }}
  </h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <!-- <ul style="overflow: hidden"> -->

  {% if member.number_educ >= 1 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education1 }}</p>
{% endif %}
{% if member.number_educ >= 2 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education2 }}</p>
{% endif %}
{% if member.number_educ >= 3 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education3 }}</p>
{% endif %}
{% if member.number_educ >= 4 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education4 }}</p>
{% endif %}
{% if member.number_educ == 5 %}
  <p style="margin: 0 0 2px 0; line-height: 1.2; color: #444;">{{ member.education5 }}</p>
{% endif %}

  {% if member.email or member.website or member.google_scholar %}
  <p style="margin-top: 1rem; font-size: 0.95em; white-space: nowrap;">
    {% if member.email %}
      <a href="mailto:{{ member.email }}">{{ member.email }}</a>
    {% endif %}
    {% if member.website %}
      {% if member.email %} | {% endif %}
      <a href="{{ member.website }}" target="_blank">Personal Website</a>
    {% endif %}
    {% if member.google_scholar %}
      {% if member.email or member.website %} | {% endif %}
      <a href="{{ member.google_scholar }}" target="_blank">Google Scholar</a>
    {% endif %}
  </p>
{% endif %}

  <!-- </ul> -->
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


<!-- ## <span style="color: #8C1D40;"><strong>PhD and Postdoc Alumni</strong></span>

{% assign number_printed = 0 %}
{% for member in site.data.alumni_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="15%" style="float: left" />
  <h4 style="font-size: 2.4rem; font-weight: 600; margin-top: 18px;">
    {{ member.name }}
  </h4>
  <i>{{ member.duration }}</i>
  
  {% if member.dissertation %}
  <i>Dissertation: {{ member.dissertation }}</i>
  {% endif %}

  {% if member.email %}
  <a href="mailto:{{ member.email }}">{{ member.email }}</a>
  {% endif %}

  {% if member.website %}
  <a href="{{ member.website }}" target="_blank">Personal Website</a>
  {% endif %}
  
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %} -->

<!-- ## <span style="color: #8C1D40;"><strong>Former visitors, BSc/ MSc students</strong></span>
<div class="row">

<div class="col-sm-4 clearfix">
<h4>Visitors</h4>
{% for member in site.data.alumni_visitors %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Master students</h4>
{% for member in site.data.alumni_msc %}
{{ member.name }}
{% endfor %}
</div>

<div class="col-sm-4 clearfix">
<h4>Bachelor Students</h4>
{% for member in site.data.alumni_bsc %}
{{ member.name }}
{% endfor %}
</div>

</div> -->

<div style="margin-bottom: 40px;"></div>
