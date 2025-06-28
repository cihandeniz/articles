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
