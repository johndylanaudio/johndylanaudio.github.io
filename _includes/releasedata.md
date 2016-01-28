{% for release in site.data.appearances %}
  {% if release.id == release_id %}
    {% assign title=release.title %}
	{% assign description=release.description %}
	{% for releasetrack in release.releasetracks %}
		{% for track in site.data.songs %}
			{% if track.id == releasetrack.id %}
				{% capture new_track %}<li><a href="/tracks/{{ track.id }}">{{ track.title }}</a></li>{% endcapture %}
				{% capture tracklist %}{{ tracklist }}
{{ new_track }}{% endcapture %}
			{% endif %}
		{% endfor %}
	{% endfor %}
  {% endif %}
{% endfor %}

## {{ title }}

{{ description }}

### Tracklist

<ol>
{{ tracklist }}
</ol>

<< <a href="/tracks/">Back to Tracks List</a><br/>
<< <a href="/releases/">Back to Release List</a>