---
layout: page
title: "Chronology"
permalink: /chronology
---

**This is a work in progress or a 'live' document charting the
significant dates -- events, publications, etc -- over a widened
timeframe around the publication of *Recherches* 13 and the work of the
CERFI 'Genealogy' group.**

{% for event in site.data.chronology %}
<div class="timeline-entry">
	<h2>{{ event.year-month }}</h2>
	{{ event.event | markdownify }}
</div>
{% endfor %}
