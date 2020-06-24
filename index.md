---
layout: page
title: "Home"
class: home
---

# Hi, I'm Suryatej Reddy

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a research assistant at [IDSS@MIT](https://idss.mit.edu/), advised by [Dr. Kiran Garimella](https://idss.mit.edu/staff/kiran-garimella/), researching misinformation/hate speech on WhatsApp while building large scale tools for visualization and analysis. In August 2020, I will start as a Member of Technical Staff at [Adobe, India](https://www.adobe.com/).

I received my B.Tech in Computer Science from [IIIT Delhi](https://iiitd.ac.in/), where I worked with [Prof. Ponnurangam Kumaraguru](https://www.iiitd.ac.in/pk) as part of [PreCog](http://precog.iiitd.edu.in/). I also had the oppurtunity to work with [Prof. Tavpritesh Sethi](https://www.iiitd.ac.in/tavpritesh), [Prof. Rajiv Ratn Shah](https://www.iiitd.ac.in/rajivratn) and [Dr. Arnab Chatterjee](https://sites.google.com/site/arnabchat/research/tcs) on various projects.

I am passionate about building live systems and software in general. I enjoy working in reserch environments where I can build tools and technologies that take research ideas into live projects (some of which are listed below).
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


