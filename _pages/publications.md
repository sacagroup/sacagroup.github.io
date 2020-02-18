---
title: "SACA - Publications"
layout: gridlay
excerpt: "SACA Group Publications."
sitemap: false
permalink: /publications/
---


# Peer-Reviewed Publication and PrePrints
{% for yr in site.data.publist %}
<h3>{{ yr.year }}</h3>
-----
{% for publi in yr.pubs %}
  <b>[{{ publi.link.display }}] </b> &nbsp;
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.title }}</a> <br /> {{ publi.description }} 

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
