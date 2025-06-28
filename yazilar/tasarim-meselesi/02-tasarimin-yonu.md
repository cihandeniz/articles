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

{% assign pages = site.pages | where: "dir", page.dir | sort: "path" %}
{% assign filtered_pages = "" | split: "" %}

{% for p in pages %}
  {% unless p.name == "index.md" %}
    {% assign filtered_pages = filtered_pages | push: p %}
  {% endunless %}
{% endfor %}

{% assign index = filtered_pages | index_of: page %}
{% assign previous = filtered_pages[index | minus: 1] %}
{% assign next = filtered_pages[index | plus: 1] %}

<nav>
  <p>↑ [{{ page.dir | split: '/' | last | replace: '-', ' ' | capitalize }}]({{ site.baseurl }}{{ page.dir }})</p>

  <p>
    {% if previous %}
      ← Önceki: [{{ previous.title }}]({{ previous.url }})
    {% endif %}
    {% if next %}
      → Sonraki: [{{ next.title }}]({{ next.url }})
    {% endif %}
  </p>
</nav>
