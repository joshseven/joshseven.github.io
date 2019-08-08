---
layout: archive
permalink: /full-stack/
title: "Full stack Posts by Tags"
author_profile: true
header:
    images: "images/water.jpeg"
---

{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
    {% assign posts = group_items [forloop.index0] %}
    <h2 id="{{ tag | slugify }}" class="archive_subtitle">{{ tag }}</h2>
    {% include archive-single.html %}
 {% endfor %}
{% endfor %}