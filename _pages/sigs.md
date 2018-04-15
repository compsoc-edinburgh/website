---
permalink: /special-interest-groups
longtitle: "Special Interest Groups"
title: "SIGs"
---

Are you and your friends interested in a particular field of Informatics? Start a SIG!

CompSoc offers SIGs promotion, some money, support, and a place on the committee. [Send us an email]({{ site.baseurl }}/contact) if you're interested in forming a SIG.

### Our SIGs
<div class="d-flex flex-wrap justify-content-center justify-content-sm-start mb-2">
    <div class="sigs-item" style="background-color: #292b2c">
        <a href="http://sigint.mx" class="d-inline-block" style="padding: 25px">
            <img src="{{ site.baseurl }}/static/img/sigs/sigint-logo.png" height="200px" class="float-left" />
        </a>
    </div>
    <a href="http://hacktheburgh.com" class="sigs-item d-flex list-group-item list-group-item-action align-items-center justify-content-center">
        <div class="d-block">
            <h1>HackSIG</h1>
            <p>Go to hackathons and throw hackathons!</p>
        </div>
    </a>
    {% for sig in page.quicksigs %}
    <a href="{{ site.baseurl }}/sigs/{{ sig.slug }}" class="sigs-item d-flex list-group-item list-group-item-action align-items-center justify-content-center">
        <div class="d-block">
            <h1>{{ sig.title }}</h1>
            <p>{{ sig.description }}</p>
        </div>
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
