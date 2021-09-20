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

<h2>Combinatorial Optimization stuff</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "copt" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Probabilistic Graphical Model stuff</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Medical Imaging stuff</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "medic" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Multi-label Classification stuff</h2>

{% for post in site.publications reversed %}
  {% if post.topic == "mlc" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

<h2>Other stuff</h2>

{% for post in site.publications reversed %}
  {% if post.topic != "mlc" and post.topic != "medic" and post.topic != "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}
