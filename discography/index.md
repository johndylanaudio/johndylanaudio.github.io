---
title: Release List
description: Every release we've put out.
---

## Discography

A complete listing of every track we've released -- and where to get it.

{% include jswidgets.html %}{{ pagetoc }}

## Release List

<table>
{% for release in site.data.appearances %}<tr><td><a href="/discography/{{ release.id }}">{{ release.title }}</a></td></tr>{% endfor %}
</table>

## Track List

<table>
{% for track in site.data.songs %}<tr><td><a href="/discography/{{ track.id }}">{{ track.title }}</a></td></tr>{% endfor %}
</table>
