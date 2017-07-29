---
title: "The Team"
has_include: true
# Note that you may also need to edit the above include
---

We are the team that brings you the best experience in all things Informatics.

{% include snippets/join-us.html %}

{% assign committee = (site.data.committee | sort) | reverse %}

<div class="row">
	<div class="col-xl-2 col-lg-3 push-lg-8 col-sm-12">
		<ul id="cohorts" class="list-group">
			{% for cohort in committee %}
				{% if cohort.year %}
					<li class="list-group-item">
						<a class="" href="#cohort-{{ cohort.year | slugify }}">{{ cohort.year }}</a>
					</li>
				{% endif %}
			{% endfor %}
		</ul>
	</div>
	<!-- -->
	<!-- -->
	<div class="col-lg-8 pull-lg-3 pull-xl-2 col-sm-12">
		{% for cohort in committee %}
			{% if cohort.year %}
			<i id="cohort-{{ cohort.year | slugify }}"></i>
			<ul class="list-group mb-4">
				<li class="list-group-item justify-content-between">
					<h5 class="mb-0">{{ cohort.year }}</h5>
					<span>
						<!--<a class="btn disabled btn-sm btn-outline-danger" href="#">Financial Report</a>-->
						{% if cohort.annual_report %}
						<a class="btn btn-sm btn-outline-danger" href="https://github.com/compsoc-edinburgh/annual-reports/blob/master/{{ cohort.year | slugify }}.pdf">Annual Report</a>
						{% endif %}
					</span>
				</li>
				{% for member in cohort.members %}
					<li class="list-group-item justify-content-between">
						<strong>{{ member.role }}</strong>
						<span>{{ member.name }}</span>
					</li>
				{% endfor %}
			</ul>
			{% endif %}
		{% endfor %}
	</div>
</div>
