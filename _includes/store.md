
## Music

<style>
.button { margin-right: 10px !important; }
</style>

{% for release in site.data.oldreleases %}{% if release.old != true and release.hidden != true %}
<h3><i>{{ release.title }}</i></h3>
{% if release.cdbaby %}<a href="{{ release.cdbaby }}" target="_blank" class="button">CD Baby</a>{% endif %}{% if release.bandcamp %}<a href="{{ release.bandcamp }}" target="_blank" class="button">Bandcamp</a>{% endif %}{% if release.itunes %}<a href="{{ release.itunes }}" target="_blank" class="button">iTunes</a>{% endif %}{% if release.google %}<a href="{{ release.google }}" target="_blank" class="button">Google</a>{% endif %}{% if release.amazon %}<a href="{{ release.amazon }}" target="_blank" class="button">Amazon</a>{% endif %}
<div style="width:100%; display:block; float:none;"><div style="width:50%; display:block; position: relative; float:left; vertical-align: top; padding: 5px">{% if release.cdbabywidget %}
<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% if release.fanclubonly == true %}<a href="{{ release.bandcamp }}" target="_blank"><img src="{{ release.image }}" style="max-width:100%"></a>{% endif %}
</div><div style="width:50%; position: relative; display:block; float:left; vertical-align: top; padding:5px;">
{% if release.youtubeembed %}<iframe width="400" height="225" src="{{ release.youtubeembed }}" frameborder="0" allowfullscreen></iframe>
{% endif %}<br>
{% if release.description %}{{ release.description | markdownify }}{% endif %}
<i>{{ release.stats }}</i>
</div>
</div>
{% if release.pressclips %}
<div style="width:100%;float: inherit;display:inline-block; padding-top:15px;"><b style='font-size:20px;'>Press for <i>{{ release.title }}</i></b>
<hr style='margin-top:15px;margin-bottom:15px'>
{{ release.pressclips | strip | markdownify }}</div>
{% endif %}
<div style="width:100%;float: inherit;display:inline-block;">&nbsp;</div>
{% endif %}
{% endfor %}



## John Dylan Fan Club for Sensitive People ($5 per month)

<a href="https://johndylan.bandcamp.com/fan-club" target="_blank" class="button">Bandcamp</a>

Members of the John Dylan Fan Club for Sensitive People receive:

- The complete discography -- everything you see here -- available in lossless 24-bit audio should you so choose
- A steady diet of exclusive fan-club-only releases, such as live recordings, rehearsals, demos, fanclub messages, rough mixes, and more!
- 25% off all general [merch bought through Bandcamp](https://johndylan.bandcamp.com/merch)
- The satisfaction of knowing you’re supporting me in a sustainable way.

There is a $5 USD/month membership fee, which is a lot cheaper than what all the upcoming singles and album will cost individually over the coming months, so [c'mon in](https://johndylan.bandcamp.com/fan-club)!

## Merch

### "Get Beyond" T-shirt

T-shirts available for men, women, and kids.
There are both light fabric and dark fabric shirts, of various colors.
Orders fulfilled by Amazon.

<table>
<tr><td align="center">
<img src="http://i.imgur.com/fuKKUEc.png" style="max-width: 200px">
<p><a href="http://amzn.to/2tpNTms" target="_blank" class="button">Dark fabric: $25 on Amazon</a></p>
</td><td align="center">
<img src="http://i.imgur.com/poj1TD4.png" style="max-width: 200px">
<p><a href="http://amzn.to/2tuW3L3" target="_blank" class="button">Light fabric: $25 on Amazon</a></p>
</td></tr>
</table>

## John's previous music projects

{% for release in site.data.oldreleases %}
{% if release.old == true %}
<h3>{{ release.artist }} - <i>{{ release.title }}</i></h3>
{% if release.cdbaby %}<a href="{{ release.cdbaby }}" target="_blank" class="button">CD Baby</a>{% endif %}{% if release.bandcamp %}<a href="{{ release.bandcamp }}" target="_blank" class="button">Bandcamp</a>{% endif %}{% if release.itunes %}<a href="{{ release.itunes }}" target="_blank" class="button">iTunes</a>{% endif %}{% if release.google %}<a href="{{ release.google }}" target="_blank" class="button">Google</a>{% endif %}{% if release.amazon %}<a href="{{ release.amazon }}" target="_blank" class="button">Amazon</a>{% endif %}
<div style="width:100%; display:block; float:none;"><div style="width:50%; display:block; position: relative; float:left; vertical-align: top; padding: 5px">{% if release.cdbabywidget %}
<div style="max-width:600px;max-height:645px;min-width:180px;"><div style="position: relative;height: 0;overflow: hidden;padding-bottom:100%;padding-top:30px;"><iframe name="square" style="position:absolute;top:0px;left:0px;width:100%;height:100%;border:0px;" src="http://widget.cdbaby.com/{{ release.cdbabywidget }}/square/light/opaque"></iframe></div></div>{% endif %}
{% if release.fanclubonly == true %}<a href="{{ release.bandcamp }}" target="_blank"><img src="{{ release.image }}" style="max-width:100%"></a>{% endif %}
</div><div style="width:50%; position: relative; display:block; float:left; vertical-align: top; padding:5px;">
{% if release.youtubeembed %}<iframe width="400" height="225" src="{{ release.youtubeembed }}" frameborder="0" allowfullscreen></iframe>{% endif %}
<br>
{% if release.description %}{{ release.description | markdownify }}{% endif %}
<i>{{ release.stats }}</i>
</div>
</div>
{% if release.pressclips %}
<div style="width:100%;float: inherit;display:inline-block; padding-top:15px;">
<b style='font-size:20px;'>Press for <i>{{ release.title }}</i></b>
<hr style='margin-top:15px;margin-bottom:15px'>
{{ release.pressclips | strip | markdownify }}
</div>
{% endif %}
<div style="width:100%;float: inherit;display:inline-block;">&nbsp;</div>
{% endif %}
{% endfor %}
