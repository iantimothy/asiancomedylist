---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
## Clubs

<ul>
{% for club in site.clubs %}
	<li><a href="{{ club.website }}" title="{{club.name}}">{{club.name}} | {{club.description}} | {{ club.location }}</a></li>
{% endfor %}
</ul>

## Comedians

<ul>
{% for comedian in site.comedians %}
	<li><a href="{{ comedian.website }}" title="{{comedian.name}}">{{comedian.name}} | {{ comedian.country }}</a></li>
{% endfor %}
</ul>