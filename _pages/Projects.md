---
layout: single
title: "Projects"
permalink: /Projects/
author: Carlos Villanueva
author_profile: true
---
<hr>
<br>
<h2>The Personal laboral Projects are:</h2>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Work_experience == "1" %}
<h5> {{CVdata.Description}} </h5>
<h7>{{CVdata.start_date}} - {{CVdata.end_date}} </h7>
<h6> {{CVdata.Information}} </h6>
<la>  {{CVdata.Condition}} </la>
<br>
<hr>
{% endif %}
{% endfor %}

<br>
<hr>
<br>
<h2>The Personal Academic Projects are:</h2>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Work_experience == "1" %}
<h5> {{CVdata.Description}} </h5>
<h7>{{CVdata.start_date}} - {{CVdata.end_date}} </h7>
<h6> {{CVdata.Information}} </h6>
<la>  {{CVdata.Condition}} </la>
<br>
<hr>
{% endif %}
{% endfor %}
