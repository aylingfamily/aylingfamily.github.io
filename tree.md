---
layout: default
title: Family Tree
---

# The Ayling Family Tree

<div class="family-tree">
  {% for generation in site.data.family.generations %}
    <div class="generation">
      <h2>{{ generation.name }}</h2>
      <div class="generation-members">
        {% for member_id in generation.members %}
          {% assign person = site.data.family.people | where: "id", member_id | first %}
          <div class="person-card">
            {% if person.image %}
            <div class="person-image">
              <img src="{{ '/assets/images/' | append: person.image | relative_url }}" alt="{{ person.name }}">
            </div>
            {% endif %}
            <div class="person-details">
              <h3><a href="{{ '/people/' | append: member_id | append: '.html' | relative_url }}">{{ person.name }}</a></h3>
              <p class="person-dates">
                {% if person.birth_date %}{{ person.birth_date | date: "%Y" }}{% endif %}
                {% if person.death_date %} - {{ person.death_date | date: "%Y" }}{% endif %}
              </p>
              {% if person.spouse %}
                {% assign spouse = site.data.family.people | where: "id", person.spouse | first %}
                <p class="spouse">Married to: <a href="{{ '/people/' | append: person.spouse | append: '.html' | relative_url }}">{{ spouse.name }}</a></p>
              {% endif %}
            </div>
          </div>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div> 