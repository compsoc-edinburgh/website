---
title: "Partners"
---

Many of our activities at CompSoc wouldn't be possible without the support we receive from our wonderful partners. We are eternally grateful for their support over the years.

Our partners get access to opportunities for advertising jobs and events, holding engaging talks at monthly Student Tech Meet-ups, and connecting with the 1000+ members of CompSoc through a variety of other events we host, like Hackathons or CTFs.

We are always welcoming new partnerships and opportunities. If you are interested in partnering with CompSoc, please reach out to us at <a href="mailto:partners@comp-soc.com">partners@comp-soc.com</a>.

{% for group in site.data.partners %}
<div class="mt-2 partners">
	{% for partner in group %}
		{% assign imgStart = partner.img | slice: 0, 4 %}
		{% assign img = partner.img %}
		{% capture width %}{% if partner.maxwidth %} style="max-width: {{ partner.maxwidth }}" {% endif %}{% endcapture %}

		{% unless imgStart == "http" %}
			{% capture img %}{{ site.baseurl }}/{{ img }}{% endcapture %}
		{% endunless %}
        <div class="partner">
		{% unless partner.url == "" %}
			<a href="{{ partner.url }}" {{ width }} title="Click to visit {{ partner.name }}'s website">
		{% endunless %}
				<img src="{{ img }}" {{ width }} alt="Logo of {{ partner.name }}">
		{% unless partner.url == "" %}
			</a>
		{% endunless %}
            <span>{{ partner.name }}</span>
        </div>
	{% endfor %}
</div>
{% endfor %}
