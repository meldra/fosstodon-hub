{% assign inc = 0 %}
{% for step in page.steps %}
1. {{ step }}
![screenshot of step {{ inc }}](/assets/images/handbook/{{ page.title | slugify }}/{{ inc }}.png){: width="400" style="margin-left:0" }
{% assign inc = inc | plus: 1 %}
{% endfor %}
