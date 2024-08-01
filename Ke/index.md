<div id="sec_nav">
{% for chapter in site.data.menus.BX1 %}
    <li>
        {{ chapter.name }}
        {% for section in chapter.sections %}
        <li>
        {{section}}
        </li>
        {% endfor %}
    </li>
{% endfor %}
</div>