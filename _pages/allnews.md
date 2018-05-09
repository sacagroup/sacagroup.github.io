---
title: "SACA - News"
layout: textlay
excerpt: "SACA Group at the University of Central Florida."
sitemap: false
permalink: /news/
---

# News

{% for article in site.data.news %}
<p>{{ article.date }} <br>
<b>{{ article.headline }}</b> <br>
<em> {{ article.descr }} </em></p>
{% endfor %}
