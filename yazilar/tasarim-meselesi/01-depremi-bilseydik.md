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
  {% if p.path contains 'yazilar/tasarim-meselesi/' and p.url != '/yazilar/tasarim-meselesi/' %}
    {% if p.url == page.url %}
- {{ p.title }}
    {% else %}
- [{{ p.title }}]({{ site.baseurl }}{{ p.url }})
    {% endif %}
  {% endif %}
{% endfor %}
