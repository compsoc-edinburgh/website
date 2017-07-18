---
title: "The Team"
---

We are the team that brings you the best experience in all things Informatics.

Interested in joining us? At our October STMU (an <abbr title="Extraordinary General Meeting">EGM</abbr>) we will be electing the:
freshers' rep, third year rep, and the fourth year rep.

<div class="row">
	<div class="col-md-4 push-md-8 col-sm-12">
		<ul id="cohorts" class="nav flex-column">
			{% for cohort in site.data.committee %}
				<li class="nav-item">
					<a class="nav-link active" href="#cohort-{{ cohort.year }}">{{ cohort.year }}</a>
				</li>
			{% endfor %}
		</ul>
	</div>
	<!-- -->
	<!-- -->
	<div class="col-md-8 pull-md-4 col-sm-12">
		{% for cohort in site.data.committee %}
		<i id="cohort-{{ cohort.year }}"></i>
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
		{% endfor %}
	</div>
</div>
