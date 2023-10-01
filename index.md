<div>
{% for post in site.posts %}
    <div>     
    <a href="{{ post.url }}">{{ post.title }}</a>
    <div>{{ post.date | date:"(%Y年%m月%d日)" }}</div>
    <div class="post-excerpt">{{post.content | truncate:100}}</p></div>
    </div>
{% endfor %}
{% if paginator.total_pages > 1 %}
    {% if paginator.previous_page %}
        <a href="./page{{ paginator.previous_page }}">< 前一页</a>
{% endif %}
{% if paginator.next_page %}
        <a href="./page{{ paginator.next_page }}">后一页 ></a>
{% endif %}
{% endif %}
</div>