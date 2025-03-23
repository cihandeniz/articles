---
title: Yazılar
---

Henüz toparladığım bir yazı yok, ama bir tane ile başlamak üzere bu siteyi
oluşturdum. Başlangıcı _Tasarım Meselesi_ oldu, yanında başka alt konuları da
getirecektir.

{% for page in site.pages %}
  {% if page.path contains 'yazilar/' and page.url != '/yazilar/' %}
  - [{{ page.title }}]({{ page.url }})
  {% endif %}
{% endfor %}
