<div id="sec_nav">
{% for chapter in site.data.menus.BX1 %}
    <li>
        {{ chapter.name }}
        {% for section in chapter.sections %}
        <li>
        <a href="{{section}}.md">{{section}}</a>
        </li>
        {% endfor %}
    </li>
{% endfor %}
</div>

<div id="sec">
<h1>集合的概念</h1>

教材分析：

学情分析：

教学目标：

重点：

难点：

教学材料：

</div>