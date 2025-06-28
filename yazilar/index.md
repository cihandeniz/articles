---
title: Yazılar
---

Henüz toparladığım bir yazı yok, ama bir tane ile başlamak üzere bu siteyi
oluşturdum. Başlangıcı _Tasarım Meselesi_ oldu, yanında başka alt konuları da
getirecektir.

{% assign pages = site.pages | where_exp: "p", "p.path contains 'yazilar/' and p.path ends_with 'index.md'" %}
{% for page in pages %}
  {% if page.url != '/yazilar/' %}
  - [{{ page.title }}]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}
