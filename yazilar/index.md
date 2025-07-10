---
title: Yazılar
---

Henüz toparladığım bir yazı yok, ama bir tane ile başlamak üzere bu siteyi
oluşturdum. Başlangıcı _Tasarlama Meselesi_ oldu, yanında başka alt konuları da
getirecektir.

{% for page in site.pages %}
  {% if page.path contains 'yazilar/' and page.path contains '/index.md' and page.url != '/yazilar/' %}
  - [{{ page.title }}]({{ site.baseurl }}{{ page.url }})
  {% endif %}
{% endfor %}
