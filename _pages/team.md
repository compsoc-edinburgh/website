---
title: "The Team"
has_include: true
# Note that you may also need to edit the above include
---

We are the team that brings you the best experience in all things Informatics.

{% include snippets/join-us.html %}

{% assign committee = site.data.committee | sort | reverse %}

<style>
	#cohorts > .active {
		color: #868e96;
	}
</style>

<div class="row">
	<div class="col">
		<div id="cohorts" class="nav nav-pills" role="tablist">
			View committees from other years:&nbsp;
			{% for cohort in committee %}{% if cohort.year %}
				{% unless forloop.first %}&nbsp;&middot;&nbsp;{% endunless %}
				<a
						data-toggle="pill"
						role="pill"
						href="#cohort-{{ cohort.year | slugify }}"
						{% if committee[0] == cohort %}
						class="active"
						aria-expanded="true"
						{% endif %}
				>{{ cohort.year | slice: 0, 4 }}</a>
			{% endif %}{% endfor %}
		</div>
	</div>
</div>
<div class="row">
	<div class="col">
		<div class="tab-content">
		{% for cohort in committee %}
			{% if cohort.year %}
			<div
				class="tab-pane fade {% if committee[0] == cohort %}show active{% endif %}"
				id="cohort-{{ cohort.year | slugify }}"
				role="tabpanel"
			>
			<ul class="list-group mb-4">
				<li class="d-flex list-group-item justify-content-between">
					<h5 class="mb-0">{{ cohort.year }}</h5>
					<span>
						<!--<a class="btn disabled btn-sm btn-outline-danger" href="#">Financial Report</a>-->
						{% if cohort.annual_report %}
						<a class="btn btn-sm btn-outline-danger" href="https://github.com/compsoc-edinburgh/annual-reports/blob/master/{{ cohort.year | slugify }}.pdf">Annual Report</a>
						{% endif %}
					</span>
				</li>
				{% for member in cohort.members %}
					<li class="d-flex list-group-item justify-content-between">
						<strong>{{ member.role }}</strong>
						<span>
							{% if member.url %}
								<a href="{{ member.url }}">{{ member.name }}</a>
							{% else %}
								{{ member.name }}
							{% endif %}
						</span>
					</li>
				{% endfor %}
			</ul>
			</div>
			{% endif %}
		{% endfor %}
		</div>
	</div>
</div>
