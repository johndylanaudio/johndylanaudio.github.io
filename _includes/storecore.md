<h3>{{ release.title }}</h3>
{% if release.amazon %}<a href="{{ release.amazon }}" target="_blank" class="button">Amazon</a>{% endif %}
{% if release.bandcamp %}<a href="{{ release.bandcamp }}" target="_blank" class="button">Bandcamp</a>{% endif %}
{% if release.itunes %}<a href="{{ release.itunes }}" target="_blank" class="button">iTunes</a>{% endif %}
{% if release.google %}<a href="{{ release.google }}" target="_blank" class="button">Google</a>{% endif %}
{% if release.cdbaby %}<a href="{{ release.cdbaby }}" target="_blank" class="button">CD Baby</a>{% endif %}
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
{% endif %}
{% if release.pressclips %}
<div style="width:100%;float: inherit;display:inline-block; padding-top:15px;"><b style='font-size:20px;'>Press for <i>{{ release.title }}</i></b>
<hr style='margin-top:15px;margin-bottom:15px'>
{{ release.pressclips | strip | markdownify }}</div>
{% endif %}
<div style="width:100%;float: inherit;display:inline-block;">&nbsp;</div>
