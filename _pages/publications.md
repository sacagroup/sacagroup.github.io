---
title: "SACA - Publications"
layout: gridlay
excerpt: "SACA Group Publications."
sitemap: false
permalink: /publications/
---


# Publications


{% for publi in site.data.publist %}

  <b>[{{ publi.link.display }}] </b> &nbsp;
  <a href="{{ publi.link.url }}">{{ publi.title }}</a><br /><em>{{ publi.authors }} </em>

{% endfor %}

# Patents

{% for pats in site.data.patents %}

  <b> {{ pats.title }} </b>
  <br /><em>{{ pats.number }} </em>

{% endfor %}