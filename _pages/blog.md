---
permalink: "/blog/"
title: "Blog"
---

We regularly hold committee meetings to discuss our plans for CompSoc.
<a class="btn btn-primary btn-sm btn-info" href="{{ site.baseurl }}/minutes" role="button">&raquo; View meeting minutes</a>

<ul>
    {% for post in site.posts %}
    <li>
        <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a>
    </li>
    {% endfor %}
</ul>