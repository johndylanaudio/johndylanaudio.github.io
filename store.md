---
title: Store
description: Because even GY!BE sells t-shirts.
nosocial: true
---

## Music

We currently have the following music releases for sale. Bandcamp downloads include HD audio 24-bit
FLAC files.

{% for release in site.data.appearances %}<a href="/releases/{{ release.id }}">{{ release.title }}</a><br/>{% endfor %}

## Multi-track masters

You can purchase the multi-track masters for our music. These have every track isolated, and also
have the effects channels and buss channels isolated. They even include the MIDI files that were
captured from V-Drums and keyboards. As good as sitting at the DAW with John; these are all
zero-snapped WAVs that include notes on what the bpm of the song is, and how many beats click
by before the song starts. Import into your fave mixing environment, and start ripping it up.

[SELLFY LINKZ]

Note: All masters were recorded in 24-bit/96khz.

## Deluxe Editions

Deluxe editions of our singles include the following:

1. All A-side/B-side songs in 24-bit/96kHz lossless FLAC format
2. All of the bonus tracks from that single in lossless FLAC format
3. The multi-track masters for the A-side/B-side songs
4. MP3 files of all of the rough mixes we ever did for the A-side/B-side songs on that single, so you can see how the song progressed. **(Exclusive to Deluxe Editions)**
5. Digital copies of the artwork masters for that single. **(Exclusive to Deluxe Editions)** 

[SELLFY LINK]


## Pre-Sungods projects

{% for release in site.data.oldreleases %}
{% if release.cdbabywidget %}<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% endfor %}