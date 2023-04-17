---
layout: default
---

{% for post in site.posts %}
<ul>
    <li><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><br />
    <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">{{ post.date | date: "%b %-d, %Y" }}</time>{% if post.author %} • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>{% endif %}
    </li>
</ul>
{% endfor %}
