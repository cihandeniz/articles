---
title: Depremi Bilseydik
---

- Depremi bir gün önce bilseydik ne yapabilirdik
- Bir hafta önce, bir ay önce, bir yıl önce?
- Gelecek depremi bilmiyor olabiliriz, ama geçmişteki depremleri şu an
  biliyoruz, erken bilseydik ne yapardık sorusu bize yarın için ne verebilir?
- Ne olursa olsun, geleceği bilmiyoruz, ama geçmişe bakıp hayatımızı yeniden
  tasarladığımızda geleceğe daha hazırlıklı olabiliriz

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

<nav>
  {% if index_page %}
    <p>↑ [{{ index_page.title }}]({{ index_page.url }})</p>
  {% endif %}

  <p>
    {% if previous %}
      ← Önceki: [{{ previous.title }}]({{ previous.url }})
    {% endif %}

    {% if next %}
      → Sonraki: [{{ next.title }}]({{ next.url }})
    {% endif %}
  </p>
</nav>
