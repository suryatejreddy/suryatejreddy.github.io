---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

{% for pub in site.data.publications %}
  {% include publication.html pub=pub %}
{% endfor %}


