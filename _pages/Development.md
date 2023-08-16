---
layout: single
title: "Academic and Professional Development"
permalink: /Development/
author: Carlos Villanueva
author_profile: true
---
<h3>Certified Academic and Professional Development</h3>
<!-- Certified knowledge that took more than a half year -->
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Certified_Published == "1" and CVdata.Academic_Advancement == "1" %}
{% if CVdata.end_date != "0"  %}
<h4> {{CVdata.Information}} </h4>
<h6> {{CVdata.Condition}} </h6>
<a>  {{CVdata.Description}} </a>
<br>
<hr>
{% endif %}
{% endif %}
{% endfor %}

<!-- Certified knowledge that took less than a half year -->
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Certified_Published == "1" and CVdata.Academic_Advancement == "1" %}
{% if CVdata.end_date == "0"  %}
<h4> {{CVdata.Information}} </h4>
<h6> {{CVdata.Condition}} </h6>
<a>  {{CVdata.Description}} </a>
<br>
<hr>
{% endif %}
{% endif %}
{% endfor %}

