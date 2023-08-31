---
layout: single
title: "Researches"
permalink: /Researches/
author: Carlos Villanueva
author_profile: true
---
<hr>
<br>
<h2>The Personal Academic Projects are:</h2>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Investigation == "1" %}
<h5> {{CVdata.Description}} </h5>
<h7>{{CVdata.start_date}} - {{CVdata.end_date}} </h7>
<h6> {{CVdata.Information}} </h6>
<la>  {{CVdata.Condition}} </la>
<br>
<hr>
{% endif %}
{% endfor %}
