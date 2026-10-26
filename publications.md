---
layout: default
title: Publications
---

# Publications

{% for publication in site.data.publications %}
<hr>
<p>
  <strong>[{{ forloop.rindex }}]</strong>
  {% for author in publication.authors -%}
    {% if author == site.author %}<strong>{{ author | escape }}</strong>{% else %}{{ author | escape }}{% endif %}{% unless forloop.last %}, {% endunless %}
  {%- endfor %}.<br>
  <em>{{ publication.title | escape }}.</em><br>
  <strong>{{ publication.journal | escape }}</strong> {{ publication.volume | escape }}{% if publication.issue %}({{ publication.issue | escape }}){% endif %}, {{ publication.pages | escape }} ({{ publication.year | escape }}).<br>
  <a href="https://doi.org/{{ publication.doi | escape }}">DOI: {{ publication.doi | escape }}</a>
</p>
{% endfor %}
<hr>

## Conference Presentations

<ul>
{% for conference in site.data.conferences %}
  <li>
    <p><strong>{{ conference.date | escape }}</strong> — <strong>{{ conference.name | escape }}</strong>, {{ conference.location | escape }}.{% if conference.title %}<br>
    {{ conference.type | escape }}: <em>“{{ conference.title | escape }}”</em>{% else %} {{ conference.type | escape }}.{% endif %}</p>
  </li>
{% endfor %}
</ul>
