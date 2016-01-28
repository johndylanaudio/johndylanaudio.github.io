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

You can purchase the multi-track masters for our music in [Open Media Framework (OMF) 
format](https://en.wikipedia.org/wiki/Open_Media_Framework_Interchange).
**You are free to create samples or remixes from these masters and sell the results commercially
without paying us royalties or asking permission.** For more information, see [the Open Source 
Music Approach](/opensource/)

[SELLFY LINKZ]

Note: All masters were recorded in 24-bit/96khz.

## Deluxe Editions

Deluxe editions of our singles include the following:

1. All A-side/B-side songs in 24-bit/96kHz lossless FLAC format
2. All of the bonus tracks from the singles in lossless FLAC format
3. The OMF files for all our new songs in 24-bit/96kHz, so so you can easily remix to your heart's content
4. MP3 files of all of the rough mixes we ever did for the A-side/B-side songs on that single, so you can see how the song progressed. **(Exclusive to Deluxe Editions)**
5. Digital copies of the artwork masters for that release. **(Exclusive to Deluxe Editions)**

It's certainly the best value for how much stuff you get. 

[SELLFY LINK]

## Merch

- Sells Posters, Clothing, Decor, Toys
- Space for users to contribute their remixes and homemade merch/videos
- Accept user reviews of fan-contributed stuff
- Have fan contributors sign up and give me their PayPal email address first, then invoice them on PayPal later for 30%
- Fan-made digital assets must be hosted by me, then I push them 70% of sales revenue
- Include live recordings/video, zines that interview us, etc
- Digital store with HD vids, 24-bit sound, mp3 version, FLAC version
- Explain our no-stream policy
- Physical copies too

## Pre-Sungods projects

{% for release in site.data.oldreleases %}
{% if release.cdbabywidget %}<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% endfor %}