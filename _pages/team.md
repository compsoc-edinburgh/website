---
title: "The Team"
---

We are the team that brings you the best experience in all things Informatics.

{% include snippets/join-us.html %}

{% assign committee = (site.data.committee | sort) | reverse %}

<div class="row">
	<div class="col-md-4 push-md-8 col-sm-12">
		<ul id="cohorts" class="nav flex-column">
			{% for cohort in committee %}
				{% if cohort.year %}
					<li class="nav-item">
						<a class="nav-link active" href="#cohort-{{ cohort.year | slugify }}">{{ cohort.year }}</a>
					</li>
				{% endif %}
			{% endfor %}
		</ul>
	</div>
	<!-- -->
	<!-- -->
	<div class="col-md-8 pull-md-4 col-sm-12">
		{% for cohort in committee %}
			{% if cohort.year %}
				<i id="cohort-{{ cohort.year | slugify }}"></i>
				<div class="card" style="margin-bottom: 25px;">
					<h3 class="card-header text-center">{{ cohort.year }}</h3>
					<div class="card-block">
						<table class="table-sm" style="margin: 0 auto;">
							<tbody>
								{% for member in cohort.members %}
								<tr>
									<th scope="row">{{ member.role }}</th>
									<td>{{ member.name }}</td>
								</tr>
								{% endfor %}
							</tbody>
						</table>
					</div>
				</div>
			{% endif %}
		{% endfor %}
	</div>
</div>
