---
title: Tasarımın Yönü
---

- Yaşanacakları tasarlayamayız, yaşananları yaşandıktan sonra ele alıp
  tasarlayabiliriz
- Dünden mülhem tasarımlarla yarını daha iyi karşılamayı umarız, yarın dün
  olduğunda tasarımlarımızı revize eder, bilinmez ile bu şekilde baş ederiz
- Tasarlama eyleminin malzemesi ve konusu her zaman geçmiştir, gelecek
  değil. Tasarlama eylemi sonucu ortaya çıkan tasarım ise geleceği
  etkiler, hatta etkilemesi beklenir, ama geleceği kesin olarak belirlemez,
  yalnızca etkiler.
- Tasarlama eylemi sanıldığının aksine ileriye değil, geriye dönük bir
  eylemdir.

{% assign pages = site.pages | sort: "path" %}
{% assign filtered_pages = "" | split: "" %}
{% assign index_page = nil %}

{% for p in pages %}
  {% if p.path contains page.dir %}
    {% if p.name == "index.md" %}
      {% assign index_page = p %}
    {% else %}
      {% assign filtered_pages = filtered_pages | push: p %}
    {% endif %}
  {% endif %}
{% endfor %}

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
