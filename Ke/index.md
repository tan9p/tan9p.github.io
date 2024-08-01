<div id="sec_nav">
{% for chapter in site.data.menus.BX1 %}
    <li>
        {{ chapter.name }}
        {% for section in chapter.sections %}
        <li>
        <a href="Ke/{{section}}.md">{{section}}</a>
        </li>
        {% endfor %}
    </li>
{% endfor %}
</div>