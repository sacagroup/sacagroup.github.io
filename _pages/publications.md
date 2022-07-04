---
title: "SACA - Publications"
layout: gridlay
excerpt: "SACA Group Publications."
sitemap: false
permalink: /publications/
---


# Peer-Reviewed Publications and PrePrints
<h3 style="color:blue;"> <u> Lead Author is a Directly Mentored Student/PostDoc or Myself</u> </h3>
{% for yr in site.data.publist %}
<h3>{{ yr.year }}</h3>
-----
{% for publi in yr.pubs %}

{% if {{publi.team}}=="True" %}
  <b style="color:blue;">[{{ publi.link.display }}] </b> &nbsp;
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.title }}</a> <br /> {{ publi.description }} 
{% else %}
 <b>[{{ publi.link.display }}] </b> &nbsp;
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.title }}</a> <br /> {{ publi.description }}
{% endif %}

{% endfor %}
{% endfor %}

# Technical Reports

{% for report in site.data.reports %}

  <b>[{{ report.link.display }}] </b> &nbsp;
  <a href="{{ report.link.url }}">{{ report.title }}</a><br /><em>{{ report.authors }} </em>

{% endfor %}

# Patents

{% for pats in site.data.patents %}

  <b> {{ pats.title }} </b>
  <br /><em>{{ pats.number }} </em>

{% endfor %}
