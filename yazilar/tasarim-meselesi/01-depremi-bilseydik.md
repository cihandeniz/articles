---
title: Depremi Bilseydik
---

- Depremi bir gün önce bilseydik ne yapabilirdik
- Bir hafta önce, bir ay önce, bir yıl önce?
- Gelecek depremi bilmiyor olabiliriz, ama geçmişteki depremleri şu an
  biliyoruz, erken bilseydik ne yapardık sorusu bize yarın için ne verebilir?
- Ne olursa olsun, geleceği bilmiyoruz, ama geçmişe bakıp hayatımızı yeniden
  tasarladığımızda geleceğe daha hazırlıklı olabiliriz

{% assign pages = site.pages | where: "dir", "/yazilar/tasarim-meselesi/" | sort: "path" %}
{% assign index = pages | index_of: page %}

{% assign previous = pages[index | minus: 1] %}
{% assign next = pages[index | plus: 1] %}

<nav>
  {% if previous %}
  ← Önceki: [{{ previous.title }}]({{ previous.url }})
  {% endif %}
  {% if next %}
  → Sonraki: [{{ next.title }}]({{ next.url }})
  {% endif %}
</nav>
