---
title: Eskizler
---

Aldığım notlar ve taslakları aşağıda listeliyorum. Zamanla yazıya dönüşmeleri
dileğiyle.

{% for page in site.pages %}
  {% if page.path contains 'eskizler/' %}
  - [{{ page.title }}]({{ page.url }})
  {% endif %}
{% endfor %}
