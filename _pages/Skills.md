---
layout: single
title: "Personal, Technical and Specialized Skills"
permalink: /Skills/
author: Carlos Villanueva
author_profile: true
---
<hr>
<br>
<h3>Uncertified (Practical) Academic and Professional Skills</h3>
<br>

<!-- Personal Skills -->
<hr>
<br>
<h4> Personal Skills </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Personal_skills == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>
<!-- Technical Skills -->
<hr>
<br>
<h4> Technical skills  </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Technical_skills == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>
<!-- Specialized softwares and tools -->
<hr>
<br>
<h4> Specialized softwares and tools  </h4>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Practice == "1" and CVdata.Specialized_Tools_and_Software == "1" %}
<la>{{CVdata.Description}},</la>
{% endif %}
{% endfor %}
<br>

