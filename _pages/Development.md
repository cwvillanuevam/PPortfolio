---
layout: single
title: "Academic and Professional Development"
permalink: /Development/
author: Carlos Villanueva
author_profile: true
---
<h1>Certified Academic and Professional Development</h1>
{% for CVdata in site.data.CSVv2 %}
{{CVdata.Information}} to {{CVdata.Condition}}
{% if CVdata.Certified_Published == "1" and CVdata.Academic_Advancement == "1" %}
<h2> {{CVdata.Information}} </h2>
<h6> {{CVdata.Condition}} </h6>
<a>  {{CVdata.Description}} </a>
<br>
<hr>
{% endif %}
{% endfor %}
<!--
<h2> Personal Information </h2>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Personal_information == "1" %}
<a> {{CVdata.Information}} : {{CVdata.Description}} | {{CVdata.Condition}}</a>
<br>
{% endif %}
{% endfor %}-->
