---
permalink: "/minutes/"
layout: page
title: "Minutes"
---

The committee holds a meeting every two weeks during term time. Meetings are usually held in Forrest Hill.

<ul>
{% for meeting in site.minutes reversed %}
	<li><a href="{{ meeting.url }}">{{ meeting.date | date: "%a, %d %B %Y" }}</a></li>
{% endfor %}
</ul>