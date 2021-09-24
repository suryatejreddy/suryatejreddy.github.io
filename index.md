---
layout: page
title: "Home"
class: home
---

# Hi, I'm Suryatej 

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am a graduate student in Computer Science at [Georgia Institute of Technology](https://www.gatech.edu/) working in the domain of Systems + Machine Learning, advised by [Dr. Joy Arulraj](https://www.cc.gatech.edu/~jarulraj/). I have prior experience building ML based software systems from ground up. Some of the tools I developed are being used by interdisciplinary researchers at MIT, IIITD and TCS Research.  

I was a research assistant at [IDSS@MIT](https://idss.mit.edu/), advised by [Dr. Kiran Garimella](https://idss.mit.edu/staff/kiran-garimella/), where I studied misinformation/hate speech on WhatsApp and built large scale tools for visualization and analysis. 

I received my B.Tech in Computer Science from [IIIT Delhi](https://iiitd.ac.in/), where I worked with [Prof. Ponnurangam Kumaraguru](https://www.iiitd.ac.in/pk) as part of [PreCog](http://precog.iiitd.edu.in/). I also had the oppurtunity to work with [Prof. Tavpritesh Sethi](https://www.iiitd.ac.in/tavpritesh), [Prof. Rajiv Ratn Shah](https://www.iiitd.ac.in/rajivratn) and [Dr. Arnab Chatterjee](https://sites.google.com/site/arnabchat/research/tcs) on various projects.

I have interned/worked at various places in both industry and academia (3 publications). I also co-ran a marketing-tech services company for a while with leading marketing agencies in India as clients where I had the opportunity to take up marketing and sales related responsibilities.
</div>

<div class="me" markdown="1">
<picture>
  <img
    src='/images/suryatej.jpeg'
    alt='Suryatej Reddy'/>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

## Live Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

## Publications

<div class="featured-publications">
  {% for pub in site.data.publications %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{{ pub.venue }}, {{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
  {% endfor %}
</div>


