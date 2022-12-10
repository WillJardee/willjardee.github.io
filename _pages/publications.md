---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

I am but a mere first year grad student in a theory field. There will be stuff here... eventually.

Check out the lab I work in: [Numerical Intelligent Systems Laboratory](https://www.cs.montana.edu/sheppard/NISL/index.html).

{% include base_path %}

{% for post in site.publications %}
  {% include archive-single.html %}
{% endfor %}
