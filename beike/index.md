<ul>
{% for page in site.pages %}
<li>
<a href="{{ page.url }}">{{ page.title }}</a>
</li>
<li>{{ page.content}}</li>
<li>{{ page.url}}</li>
<li>{{ page.date}}</li>
<li>{{ page.categories}}</li>
<li>{{ page.name}}</li>
<li>{{ page.path}}</li>
{% endfor %}
</ul>