---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

<ul>
{% for item in site.data.navigation.main %}
  <li><a href="{{ item.url | relative_url }}">{{ item.title }}</a></li>
{% endfor %}
</ul>

{% for collection in site.collections %}
  {% if collection.output and collection.docs.size > 0 %}
    <h2>{{ collection.label | capitalize }}</h2>
    {% for post in collection.docs %}
      {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% endfor %}

[XML sitemap]({{ '/sitemap.xml' | relative_url }})
