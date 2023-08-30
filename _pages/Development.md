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

<h3>Uncertified (Practical) Academic and Professional Skills</h3>
<!-- Personal Skills -->
<h4> Personal Skills </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Personal_skills == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>
<!-- Technical Skills -->
<h4> Technical skills  </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Technical_skills == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>
<!-- Specialized softwares and tools -->
<h4> Specialized softwares and tools  </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Specialized_Tools_and_Software == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>

