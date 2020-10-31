---
permalink: /special-interest-groups
longtitle: "Special Interest Groups"
title: "SIGs"
---

Are you and your friends interested in a particular field of Informatics? Start a SIG!

CompSoc offers SIGs promotion, some money, support, and a place on the committee. [Send us an email](mailto:hello@comp-soc.com?subject=Forming%20a%20new%20SIG) if you're interested in forming a SIG.

### Our SIGs
<div class="sigs__grid">
    {% for sig in site.data.sigs %}
        {% if sig.url %}
            {% assign sighref = sig.url %}
        {% else %}
            {% capture sighref %} {{ site.baseurl }}/sigs/{{ sig.slug }} {% endcapture %}
        {% endif %}
    <a href="{{ sighref }}" class="sigs__sig">
        <div class="sigs__sigtext">
            <h1>{{ sig.title }}</h1>
            <p>{{ sig.description }}</p>
        </div>
        {% if sig.image %}
        <img src="{{ site.baseurl }}/static/img/sigs/{{ sig.slug }}.png" class="sigs__img"
                                                                         style="background-color: {{ sig.colour }}; border-radius: {{ sig.radius }}"/>
        {% endif %}
    </a>
    {% endfor %}
</div>

### Defunct SIGs
We have previously had special interest groups in these subject areas:
<ul>
    <li>Audio Engineering</li>
    <li>Electrical Engineering</li>
    <li>Robotics</li>
</ul>

**Note:** Given enough interest, defunct SIGs have the possibility of being revived. If you feel like you would want to do so, [let us know]({{ site.baseurl }}/contact)!
