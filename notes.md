---
layout:     page
title: "Notes"
date: 2017-02-16
modified:  2017-04-11
permalink: /notes/
summary:    "Personal research notes."
---

{% for note in site.notes %}
  <p><a href="{{ note.url  | absolute_url  }}">{{ note.title | smartify }}
</a>{% if note.date %}, {{ note.date | date_to_string }}{% endif %}{% if note.modified %} (Modified {{ note.modified | date_to_string }}){% endif %}</p>
{% endfor %}


{% for album in site.albums %}
  <h2>{{ album.title }}</h2>
  <p>Performed by {{ album.artist }}{% if album.director %}, directed by {{ album.director }}{% endif %}</p>
  {% for work in album.works %}
    <h3>{{ work.title }}</h3>
    <p>Composed by {{ work.composer }}</p>
    <ul>
    {% for track in work.tracks %}
      <li>{{ track.title }} ({{ track.duration }})</li>
    {% endfor %}
    </ul>
  {% endfor %}
{% endfor %}
