---
title: "MARGIN Lab - Publications"
layout: gridlay
excerpt: "MARGIN Lab -- Publications."
sitemap: false
permalink: /publications/
---

## <span style="color: #8C1D40;"><strong>Recent Work</strong></span>

<!-- **Jump to the [full list of publications and patents](#full-list-of-publications).** -->

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-12 clearfix">
<img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="30%" style="float: left" />
 <div class="well">
  <pubtit>
    <a href="{{ publi.link.url }}" target="_blank">{{ publi.title }}</a>
  </pubtit>
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong>{{ publi.link.display }}</strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>


<!-- ## Patents
<em>Milan P Allan, S Gröblacher, RA Norte, M Leeuwenhoek</em><br />Novel atomic force microscopy probes with phononic crystals<br /> PCT/NL20-20/050797 (2020)

<em>Milan P Allan</em><br /> Methods of manufacturing superconductor and phononic elements <br /> <a href="https://patents.google.com/patent/US10439125B2/en?inventor=Milan+ALLAN&oq=inventor:(Milan+ALLAN)">US10439125B2 (2016)</a> -->

## Full List of publications

{% for publi in site.data.publist %}

  <a href="{{ publi.link.url }}" target="_blank">{{ publi.title }}</a><br />
  <em>{{ publi.authors }}</em><br />
  {{ publi.link.display }}

{% endfor %}

<div style="margin-bottom: 28px;"></div>
