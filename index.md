---
layout: default
title: Home
---

# Welcome to the Ayling Family History

This website is dedicated to preserving and sharing the history of the Ayling family. Here you'll find information about family members, stories, photos, and our family tree.

## Recent Additions

* [John Ayling's profile](/people/john_ayling.html) has been updated with new photos
* Added memories from the 1975 family reunion
* New section about the Ayling family origins in England

## Explore the Family Tree

{% for generation in site.data.family.generations %}
<h3>{{ generation.name }}</h3>
<ul class="generation-list">
  {% for member_id in generation.members %}
    {% assign person = site.data.family.people | where: "id", member_id | first %}
    <li><a href="{{ '/people/' | append: member_id | append: '.html' | relative_url }}">{{ person.name }}</a></li>
  {% endfor %}
</ul>
{% endfor %}

## About This Site

This site was created to preserve our family history for future generations. If you're a family member and would like to contribute stories, photos, or information, please contact us. 