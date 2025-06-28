---
title: Tasarım Meselesi
---

## İçindekiler

{% for page in site.pages %}
  {% if page.path contains 'yazilar/tasarim-meselesi/' and page.url != '/yazilar/tasarim-meselesi/' %}
  - [{{ page.title }}]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}
