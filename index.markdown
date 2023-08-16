---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
header:
  overlay_image: /_Images/HomeImg.png
  overlay_filter: linear-gradient(rgba(0, 255, 255, 0.5), rgba(95, 0, 95, 0.5))
  caption: "Image generated with AI: [**Microsoft Designer**](https://designer.microsoft.com/invite) & [**Draw.io**](https://app.diagrams.net/)"
  actions:
    - label: "More Info"
      url: "https://github.com/cwvillanuevam/PPortfolio/"
author_profile: false
---
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Aim == "1" %}
<h2> {{CVdata.Information}} </h2>
<h6> {{CVdata.Condition}} </h6>
<a>  {{CVdata.Description}} </a>
<br>
<hr>
{% endif %}
{% endfor %}

<h2> Personal Information </h2>
{% for CVdata in site.data.CSVv2 %}
{% if CVdata.Personal_information == "1" %}
<a> {{CVdata.Information}} : {{CVdata.Description}} | {{CVdata.Condition}}</a>
<br>
{% endif %}
{% endfor %}


