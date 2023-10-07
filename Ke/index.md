<div>
{% for chapter in site.data.menus.BX1.chapters %}
    <li>
        {{ chapter }}
        {% for section in chapter %}
        <li>
        {{section}}
        </li>
        {% endfor %}
    </li>
{% endfor %}
</div>