---
title: Events
order: 5
---

## Upcoming Ripley & Lambert events

{% for post in site.events %}
<article>
<h3>{{ post.title }}</h3>

<img src="{{ post.image }}" title="{{ post.title }}">

<p>with <a href="{{ post.speakersite }}">{{ post.speaker }}</a></p>

<p><strong>{{ post.date | date_to_long_string: "ordinal" }}</strong></p>

<p>{{ post.time }}</p>

{{ post.content | markdownify }}

</article>
{% endfor %}

{% if site.pasts.size > 0 %}

## Postponed events at Ripley & Lambert

{% for post in site.regular %}
<article>
<h3>{{ post.title }}</h3>

<img src="{{ post.image }}" title="{{ post.title }}">

<p>with <a href="{{ post.speakersite }}">{{ post.speaker }}</a></p>

<p><strong>{{ post.date | date_to_long_string: "ordinal" }}</strong></p>

<p>{{ post.time }}</p>

{{ post.content | markdownify }}

</article>
{% endfor %}

## Previous events at Ripley & Lambert
{% endif %}

{% for post in site.pasts %}
<article>
<h3>{{ post.title }}</h3>

<img src="{{ post.image }}" title="{{ post.title }}">

<p>with <a href="{{ post.speakersite }}">{{ post.speaker }}</a></p>

<p><strong>{{ post.date | date_to_long_string: "ordinal" }}</strong></p>

<p>{{ post.time }}</p>

{{ post.content | markdownify }}

</article>
{% endfor %}
