---
layout: archive
title: "Open Source"
permalink: /open-source/
author_profile: true
---

I contribute to open-source projects that are widely used by developers and communities. I enjoy small, careful improvements that make tools easier to use, more reliable, or better documented.

{% include base_path %}

{% assign categories = "Microsoft Ecosystem|Artificial Intelligence & Machine Learning|Cloud Infrastructure & DevOps|Research & Education" | split: "|" %}
{% for cat in categories %}
{% assign cat_items = site.open_source | where: "category", cat | sort: "order" %}
{% if cat_items.size > 0 %}
## {{ cat }}

{% for post in cat_items %}
  {% include archive-single.html %}
{% endfor %}

{% endif %}
{% endfor %}

## Profiles

- **GitHub**: https://github.com/mohiuddin-khan-shiam
- **LinkedIn**: https://www.linkedin.com/in/s-m-mohiuddin-khan-shiam/
- **Hugging Face**: https://huggingface.co/mohiuddin-khan-shiam
- **Kaggle**: https://www.kaggle.com/smmohiuddinkhanshiam

If you’d like to collaborate on open-source work, feel free to reach out via the [Contact]({{ '/contact/' | relative_url }}) page.
