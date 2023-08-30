---
layout: single
title: "Academic and Professional Development"
permalink: /Development/
author: Carlos Villanueva
author_profile: true
---
<hr>
<br>
<h3>Certified Academic and Professional Development</h3>
<br>
<hr>
<!-- Certified knowledge that took more than a half year -->
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Certified_Published == "1" and CVdata.Academic_Advancement == "1" %}
{% if CVdata.end_date != "0"  %}
<h5> {{CVdata.Description}} </h5>
<h7>{{CVdata.start_date}} - {{CVdata.end_date}} </h7>
<h6> {{CVdata.Information}} </h6>
<a>  {{CVdata.Condition}} </a>
<br>
<hr>
{% endif %}
{% endif %}
{% endfor %}

<!-- Certified knowledge that took less than a half year -->
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Certified_Published == "1" and CVdata.Academic_Advancement == "1" %}
{% if CVdata.end_date == "0"  %}
<h5> {{CVdata.Information}} </h5>
<h6> {{CVdata.Condition}} </h6>
<a>  {{CVdata.Description}} </a>
<br>
<hr>
{% endif %}
{% endif %}
{% endfor %}