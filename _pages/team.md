---
title: "The Team"
---

We are the team that brings you the best experience in the field of Computer Science.

Interested in joining us? At our October STMU (an <abbr title="Extraordinary General Meeting">EGM</abbr>) we will be electing the:
freshers' rep, third year rep, and the fourth year rep.


{% for cohort in site.data.committee %}
## {{ cohort.year }}

<ul>
	{% for member in cohort.members %}
		<li>
			<strong>{{ member.name }}</strong> - <em>{{ member.role }}</em>
		</li>
	{% endfor %}
</ul>
{% endfor %}
