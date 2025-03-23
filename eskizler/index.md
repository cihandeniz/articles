---
title: Eskizler
---

Aldığım notlar ve taslakları aşağıda listeliyorum. Zamanla yazıya dönüşmeleri
dileğiyle.

{% for page in site.pages %}
  {% if page.path contains 'eskizler/' and page.url != '/eskizler/' %}
  - [{{ page.title }}]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}
