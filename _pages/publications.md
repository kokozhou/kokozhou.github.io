---
layout: publication
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">
    You can also find my articles on
    <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.
  </div>
{% endif %}

<h2>All Publications</h2>

{% for post in site.publications reversed %}
  <div class="publication-container">
    <div class="publication-image">
      {% if post.image %}
        <img src="{{ post.image }}" alt="Main image for {{ post.title }}">
      {% endif %}
      {% if post.additional_images %}
        {% for extra_img in post.additional_images limit: 1 %}
          <img src="{{ extra_img }}" alt="Extra image for {{ post.title }}">
        {% endfor %}
      {% endif %}
    </div>
    <div class="publication-text">
      <!-- Link to internal page -->
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.description }}</p>

      <!-- Optional download button -->
      {% if post.paperurl %}
        <p><a href="{{ post.paperurl }}" class="btn" target="_blank" rel="noopener">Download the Paper</a></p>
      {% endif %}

      <!-- Optional external journal link -->
      {% if post.external_url %}
        <p><a href="{{ post.external_url }}" target="_blank" rel="noopener">View on Journal Website</a></p>
      {% endif %}
    </div>
  </div>
{% endfor %}
