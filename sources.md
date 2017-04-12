---
layout: page
title: Sources
modified: 2017-04-11
permalink: /sources/
---

{% for source in site.sources %}
  <p><a href="{{ source.url  | absolute_url  }}">{{ source.title | smartify }}</a>
{% if source.date %}, {{ source.date | date_to_string }}{% endif %}{% if source.modified %} (Modified {{ source.modified | date_to_string }}){% endif %}</p>
{% endfor %}
