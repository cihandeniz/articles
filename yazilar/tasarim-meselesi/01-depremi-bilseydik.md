---
title: Depremi Bilseydik
---

- Depremi bir gün önce bilseydik ne yapabilirdik
- Bir hafta önce, bir ay önce, bir yıl önce?
- Gelecek depremi bilmiyor olabiliriz, ama geçmişteki depremleri şu an
  biliyoruz, erken bilseydik ne yapardık sorusu bize yarın için ne verebilir?
- Ne olursa olsun, geleceği bilmiyoruz, ama geçmişe bakıp hayatımızı yeniden
  tasarladığımızda geleceğe daha hazırlıklı olabiliriz

---

## İçindekiler

{% for p in site.pages %}
  {% if p.path contains 'yazilar/' and p.path contains '/index.md' and p.url != '/yazilar/' %}
    {% if p.url == page.url %}
- [{{ p.title }}]({{ site.baseurl }}{{ p.url }})
    {% elsif %}
- {{ p.title }}
    {% endif %}
  {% endif %}
{% endfor %}
