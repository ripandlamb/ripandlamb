---
title: Events
order: 5
---

## Upcoming events at Ripley & Lambert

{% for post in site.events %}
### {{ post.title }}

![{{ post.title }}]({{ post.image }})

with [{{ post.speaker }}]({{ post.speakersite }})

**{{ post.date | date_to_long_string: "ordinal" }}**

{{ post.time }}

{{ post.content }}

{% endfor %}

## Previous events at Ripley & Lambert

{% for post in site.pasts %}
### {{ post.title }}
with [{{ post.speaker }}]({{ post.speakersite }})

**{{ post.date | date_to_long_string: "ordinal" }}**
{{ post.time }}

![{{ post.title }}]({{ post.image }})

{{ post.content }}

{% endfor %}