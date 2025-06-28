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

{% assign pages = site.pages | where: "dir", page.dir | sort: "path" %}

{%- assign filtered_pages = "" | split: "" -%}
{%- assign index_page = nil -%}

{%- for p in pages -%}
  {%- if p.name == "index.md" -%}
    {%- assign index_page = p -%}
  {%- else -%}
    {%- assign filtered_pages = filtered_pages | push: p -%}
  {%- endif -%}
{%- endfor -%}

{% assign index = filtered_pages | index_of: page %}
{% assign previous = filtered_pages[index | minus: 1] %}
{% assign next = filtered_pages[index | plus: 1] %}

{% if index_page %}
↑ Yukarı: [{{ index_page.title }}]({{ index_page.url }})
{% endif %}

{% if previous %}
← Önceki: [{{ previous.title }}]({{ previous.url }})
{% endif %}

{% if next %}
→ Sonraki: [{{ next.title }}]({{ next.url }})
{% endif %}
