---
title: Photo Gallery
layout: default
---
<div id="photo-gallery">
    {% assign sorted_pages = site.pages | sort: 'path' %}
    {% for page in sorted_pages %}
    {% if page.layout == 'gallery' %}
    <a href="{{page.url}}">
        <img src="//i{% cycle '0', '1', '2' %}.wp.com/{{site.domain}}{{page.gallery[0]}}?resize=176,132" alt="" height="132" width="176" />
        <h3>{{page.title}}</h3>
    </a>
    {% endif %}
    {% endfor %}
</div>