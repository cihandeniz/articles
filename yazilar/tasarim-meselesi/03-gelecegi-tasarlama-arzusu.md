---
title: Geleceği Tasarlama Arzusu
---

- Gelecek korkusu ve bu korkudan hareketle belirsizliği giderme arzusu
- Geleceğin belirsizliğinin verdiği bireysel/toplumsal kaygılar
- Tanrı'nın her şeyi bilmesi, İsa'nın geleceği mitlerinin adreslediği
  kaygılar bunlar
- Tanrı bize ebeveynlik yapıyor, ve bu korkularımızın bizi ele geçirmesini
  engelliyor diye düşünebiliriz
- Büyüdüğümüzde, hala ebeveynlik ihtiyacı zaman zaman duymakla beraber,
  bilinmezlikle başa çıkmakta daha iyi olmamız gerekir (ya da beklenir), çünkü
  onu göğüsleyen artık büyüklerimiz değil, bizizdir.
- Geleceğe dair duyabileceğimiz tek duygu korku olmak değil. Korku yerine
  güven duygusu üzerinden geleceği karşılayabilir ve inşa edebiliriz.
  - Bu güven (trust değil, confidence), gelecekte olacak şeyleri
    etkileyebileceğimize olan inancımızdır. (Joe)

{% assign yazilar = site.pages | where: "dir", "/yazilar/" | sort: "path" %}
{% assign index = yazilar | index_of: page %}

{% assign previous = yazilar[index | minus: 1] %}
{% assign next = yazilar[index | plus: 1] %}

<nav>
  {% if previous %}
  ← Önceki: [{{ previous.title }}]({{ previous.url }})
  {% endif %}
  {% if next %}
  → Sonraki: [{{ next.title }}]({{ next.url }})
  {% endif %}
</nav>
