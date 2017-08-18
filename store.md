---
title: Store
description: Because even GY!BE sells t-shirts.
nosocial: true
---

## Music

{% for release in site.data.oldreleases %}{% if release.old != true and release.hidden != true %}
<h2>{{ release.title }}</h2>
<table><tr><td width="50%" style="vertical-align: top">{% if release.cdbabywidget %}
<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% if release.fanclubonly == true %}<a href="{{ release.bandcamp }}" target="_blank"><img src="{{ release.image }}" style="max-width:100%"></a>{% endif %}
</td>
<td width="50%" style="vertical-align: top">
{% if release.youtubeembed %}<iframe width="400" height="225" src="{{ release.youtubeembed }}" frameborder="0" allowfullscreen></iframe>{% endif %}
{% if release.description %}<p>{{ release.description | markdownify }}</p>{% endif %}
<ul>
{% if release.amazon %}<li><a href="{{ release.amazon }}" target="_blank">Amazon</a><br></li>{% endif %}
{% if release.bandcamp %}<li><a href="{{ release.bandcamp }}" target="_blank">Bandcamp</a><br></li>{% endif %}
{% if release.itunes %}<li><a href="{{ release.itunes }}" target="_blank">iTunes</a><br></li>{% endif %}
{% if release.google %}<li><a href="{{ release.google }}" target="_blank">Google</a><br></li>{% endif %}
</ul>
</td>
</tr>
</table>
{% endif %}{% endfor %}

### Open Source Music Volume 1: Get Beyond



<iframe style="border: 0; width: 350px; height: 786px;" src="https://bandcamp.com/EmbeddedPlayer/album=2444436466/size=large/bgcol=ffffff/linkcol=0687f5/transparent=true/" seamless><a href="http://johndylan.bandcamp.com/album/open-source-music-volume-1-get-beyond">Open Source Music Volume 1: Get Beyond by John Dylan</a></iframe>

## John Dylan Fan Club for Sensitive People

[**johndylan.bandcamp.com/fan-club**](https://johndylan.bandcamp.com/fan-club)

Members of the John Dylan Fan Club for Sensitive People receive:

- A steady diet of exclusive tracks early demos/takes, rehearsal recordings, live recordings, interviews, fan-club-only messages, and special recordings
- Free copy of "Open Source Music Volume 1: Get Beyond" when joining
- 15% off all general [merch bought through Bandcamp](https://johndylan.bandcamp.com/merch)
- Access to fan club-only merch
- All the new music I make streaming instantly on your mobile device via the free Bandcamp app, and also available as a high-quality download, for as long as you're a member.
- Fan Club Exclusive album: Inside "Get Beyond," covering the evolution of the song from voice memo, to demo, to rough mixes
- The satisfaction of knowing you’re supporting me in a sustainable way.

There is a $5 USD/month membership fee, which is a lot cheaper than what all the upcoming singles and album will cost invidually over the coming months, so c'mon in!

[**johndylan.bandcamp.com/fan-club**](https://johndylan.bandcamp.com/fan-club)

## Merch

### "Get Beyond" T-shirt

T-shirts available for men, women, and kids.
There are both light fabric and dark fabric shirts, of various colors.
Orders fulfilled by Amazon.

<table><tr><td align="center">
<img src="http://i.imgur.com/fuKKUEc.png" style="max-width: 200px">
<p><a href="http://amzn.to/2tpNTms">Dark fabric: $25 on Amazon</a></p>
</td><td align="center">
<img src="http://i.imgur.com/poj1TD4.png" style="max-width: 200px">
<p><a href="http://amzn.to/2tuW3L3">Light fabric: $25 on Amazon</a></p>
</td></tr></table>

## John's previous music projects

{% for release in site.data.oldreleases %}
{% if release.cdbabywidget and release.old == true %}<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% endfor %}
