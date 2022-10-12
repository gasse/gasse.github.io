---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<h2>Combinatorial Optimization</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "copt" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Probabilistic Graphical Model</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Medical Imaging</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "medic" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Multi-label Classification</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "mlc" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>PhD thesis</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "phdthesis" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Other</h2>

{% for post in site.publications reversed %}
  {% if post.topic != "phdthesis" and post.topic != "copt" and post.topic != "mlc" and post.topic != "medic" and post.topic != "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}
