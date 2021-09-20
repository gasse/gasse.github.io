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

Combinatorial Optimization stuff

{% for post in site.publications reversed %}
  {% if post.topic == "copt" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

Probabilistic Graphical Model stuff

{% for post in site.publications reversed %}
  {% if post.topic == "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

Medical Imaging stuff

{% for post in site.publications reversed %}
  {% if post.topic == "medic" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

Multi-label Classification stuff

{% for post in site.publications reversed %}
  {% if post.topic == "mlc" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}

Other stuff

{% for post in site.publications reversed %}
  {% if post.topic != "mlc" and post.topic != "medic" and post.topic != "pgms" %}
    {% include publication.html %}
  {% endif %}
{% endfor %}
