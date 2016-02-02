---
title: Release List
description: Every release we've put out.
---

## Release List
{% for release in site.data.appearances %}<a href="/releases/{{ release.id }}">{{ release.title }}</a><br/>{% endfor %}

## Track List
{% for track in site.data.songs %}<a href="/tracks/{{ track.id }}">{{ track.title }}</a><br/>{% endfor %}
