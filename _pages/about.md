---
permalink: /
title: "About me"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---
I am a systems scientist in sustainable urban environment decision-making. My research integrates complex systems interactions into strategic management and public policies. I use interdisciplinary approaches and systems science methods, including systems mapping and modelling. My work spans environmental issues, including social housing, urban regeneration, water neutrality, climate change mitigation and adaptation, and health equity. I collaborate widely with experts in environmental engineering, public health, policy, and management to engage decision-makers and policymakers in achieving healthy and sustainable outcomes.

My recent publication
======
Please find my recent publication: [Systems Thinking in Water Neutrality Governance: Moving from system failures to resilient urban water systems](https://www.sciencedirect.com/science/article/pii/S0959652625010054)

{% assign latest_post = site.posts | sort: 'date' | reverse | first %}
### Latest Blog Post
[{{ latest_post.title }}]({{ latest_post.url }})

### Latest Publications

{% for latest_pub in site.publications | sort: 'date' | reverse | limit: 3 %}
<div class="publication-container">
  <div class="publication-image">
    {% if latest_pub.image %}
      <img src="{{ latest_pub.image }}" alt="{{ latest_pub.title }}">
    {% endif %}
  </div>
  <div class="publication-text">
    <h3><a href="{{ latest_pub.url }}">{{ latest_pub.title }}</a></h3>
    <p>{{ latest_pub.description }}</p>
  </div>
</div>
{% endfor %}
