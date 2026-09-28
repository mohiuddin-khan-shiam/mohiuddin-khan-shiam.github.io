---
layout: archive
title: "Open Source Contributions"
permalink: /open-source/
author_profile: true
---

{% include base_path %}

<div class="page-intro-box">
  <p>
    <strong>Active contributor to 11+ global open-source organizations across 17+ mission-critical repositories powering millions of developers.</strong>
    My open-source work emphasizes developer experience, core machine learning estimators, edge vision models, and distributed cloud workflows.
  </p>
  <div class="research-links-bar">
    <a href="https://github.com/mohiuddin-khan-shiam" target="_blank" rel="noopener noreferrer" class="badge-link"><i class="fab fa-github"></i> GitHub Profile</a>
    <a href="https://huggingface.co/mohiuddin-khan-shiam" target="_blank" rel="noopener noreferrer" class="badge-link"><i class="fas fa-robot"></i> Hugging Face</a>
    <a href="https://kaggle.com/smmohiuddinkhanshiam" target="_blank" rel="noopener noreferrer" class="badge-link"><i class="fab fa-kaggle"></i> Kaggle</a>
    <a href="https://rosalind.info/users/shiam/" target="_blank" rel="noopener noreferrer" class="badge-link"><i class="fas fa-dna"></i> Rosalind</a>
  </div>
</div>

{% assign categories = "Microsoft Ecosystem|Artificial Intelligence & Machine Learning|Cloud Infrastructure & DevOps|Scientific Research & Education" | split: "|" %}
{% for cat in categories %}
{% assign cat_items = site.open_source | where: "category", cat | sort: "order" %}
{% if cat_items.size > 0 %}
<div class="category-header-wrap">
  <h2 class="archive__subtitle category-title">{{ cat }}</h2>
</div>

{% for post in cat_items %}
  {% include archive-single.html %}
{% endfor %}

{% endif %}
{% endfor %}

<div class="card-callout">
  <h3>Collaborations & Inquiries</h3>
  <p>
    Whether you are looking to collaborate on upstream open-source frameworks, benchmark deep learning architectures, or integrate edge AI solutions, please connect via the <a href="{{ '/contact/' | relative_url }}">Contact page</a>.
  </p>
</div>
