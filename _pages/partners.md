---
title: "Partners"
---

Here at CompSoc we are supported by some great companies that are passionate about engaging in student life.
We are eternally grateful for their support over the years.

We're currently updating our partner list for the 2017-2018 academic year. Please check back after freshers' week to see who we'll be working with this year!

<div class="partners">
	{% for partner in site.data.partners %}
		{% assign imgStart = partner.img | slice: 0, 4 %}
		{% assign img = partner.img %}

		{% unless imgStart == "http" %}
			{% capture img %}{{ site.baseurl }}/{{ img }}{% endcapture %}
		{% endunless %}

		{% unless partner.url == "" %}
			<a href="{{ partner.url}}">
		{% endunless %}
				<img src="{{ img }}">
		{% unless partner.url == "" %}
			</a>
		{% endunless %}
	{% endfor %}
</div>
