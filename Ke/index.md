<div>
{% for chapter in site.data.sections.BX1.chapters %}
    <li>
        {{chapter.name}}
        {% for section in chapter.sections %}
        <li>
        {{section.name}}
        </li>
        {% endfor %}
    </li>
{% endfor %}
</div>