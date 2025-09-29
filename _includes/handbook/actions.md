{% assign inc = 0 %}
{% for cat in page.category %}
{% assign guides = site.handbook
| sort: "weight"
| where: "category", page.category[inc] | where: "category", "actions" %}
{% if inc > 0 %}
{{ cat | capitalize }}
{% endif %}
{% for guide in guides %}
- [{{ guide.title }}]({{ guide.url }})
{% endfor %}
{% assign inc = inc | plus: 1 %}
{% endfor %}
