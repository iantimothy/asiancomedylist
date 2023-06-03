---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
## Clubs

{% assign countries = "Singapore" | split: "," %}
{% for country in countries %}
  <h3>{{ country }}</h3>
  <ul>
  {% for club in site.clubs %}
    {% if club.country == country %}
      <li><a href="{{ club.website }}" title="{{club.name}}">{{club.name}} | {{club.description}}</a></li>
    {% endif %}
  {% endfor %}
  </ul>
{% endfor %}

## Comedians

<ul>
{% for comedian in site.comedians %}
	<li><a href="{{ comedian.website }}" title="{{comedian.name}}">{{comedian.name}} | {{ comedian.country }}</a></li>
{% endfor %}
</ul>

## Specials

<ul>
{% for special in site.specials %}
	<li><a href="{{ special.website }}" title="{{special.name}}">{{special.name}} by {{ special.comedian }}</a></li>
{% endfor %}
</ul>