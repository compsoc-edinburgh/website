---
permalink: "/minutes/"
title: "Minutes"
---

The committee holds a meeting every two weeks during term time. Meetings are usually held in Forrest Hill.

<div class="d-flex flex-wrap justify-content-md-center">
{% for meeting in site.minutes reversed %}
	<a href="{{ site.baseurl }}{{ meeting.url }}" class="list-group-item list-group-item-action" style="width: 10rem; padding: 0; margin-right: 5px; margin-bottom: 5px;">
		<div class="card-block">
			<h4 class="card-title">
				{{ meeting.date | date: "%d %b" }}
			</h4>
			<p class="card-text">
				{{ meeting.date | date: "%a, %Y" }}
			</p>
		</div>
	</a>
{% endfor %}
</div>
