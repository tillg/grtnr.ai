---
layout: default
---

{% for post in site.posts %}
<ul>
    <li><h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3><br />
    <time datetime="{{ page.date | date_to_xmlschema }}" itemprop="datePublished">{{ page.date | date: "%b %-d, %Y" }}</time>{% if page.author %} • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ page.author }}</span></span>{% endif %}
    </li>
</ul>
{% endfor %}
