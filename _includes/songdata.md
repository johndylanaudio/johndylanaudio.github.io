{% for track in site.data.songs %}
	{% if track.id == song_id %}
		{% assign lyrics=track.lyrics %}
		{% assign year=track.year %}
		{% if track.isolation_of %}
			{% assign isolation_of=track.isolation_of %}
			{% assign has_lyrics=track.has_lyrics %}
		{% endif %}
	{% endif %}
{% endfor %}
{% for release in site.data.appearances %}
  {% for track in release.releasetracks %}
    {% if track.id == song_id %}
	  {% capture new_appearance %}<a href="/releases/{{ release.id }}">{{ release.title }}</a><br/>{% endcapture %}
	  {% capture appears_on %}{{ appears_on }}{{ new_appearance }}{% endcapture %}
    {% endif %}
  {% endfor %}
{% endfor %}

## {{ page.title }}

{% if isolation_of %}
	{% for track in site.data.songs %}
	  {% if track.id == isolation_of %}
	    {% assign year = track.year %}
		{% assign isolation_title = track.title %}
		{% if has_lyrics %}{% assign lyrics=track.lyrics %}{% endif %}
	  {% endif %}
	{% endfor %}
Multi-track isolation from the song "<a href="/tracks/{{ isolation_of }}">{{ isolation_title }}</a>."
{% endif %}

{% if has_lyrics != false %}
### Lyrics

{{ lyrics|newline_to_br }}

<span style="font-size:12px">Lyrics and music copyright (c) {{ year }} John Dylan</span>
{% endif %}

### Appears on

{{ appears_on }}

{% for track in site.data.songs %}
  {% if track.isolation_of == song_id %}
    {% capture new_isolation %}<li><a href="/tracks/{{ track.id }}">{{ track.title }}</a></li>{% endcapture %}
	{% capture isolations %}{{ isolations }}{{ new_isolation }}{% endcapture %}
  {% endif %}
{% endfor %}

{% if isolations %}

### Multitrack Isolations

You can download the following multitrack isolations for "{{ page.title }}," sample them, or create remixes
of them, and you are free to release the results commercially. For more information, see
[the Open Source Music Approach](/opensource/).

<ul>
{{ isolations }}
</ul>

{% endif %}