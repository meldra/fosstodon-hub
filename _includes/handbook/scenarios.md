{% assign guides = site.handbook
| sort: "weight"
| where: "category", page.category[1] | where: "category", "scenarios" %}
{% for guide in guides %}
- [{{ guide.title }}]({{ guide.url }})
{% endfor %}
