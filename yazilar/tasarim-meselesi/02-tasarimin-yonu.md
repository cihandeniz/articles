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

---

## İçindekiler

{% for p in site.pages %}
  {% if p.path contains 'yazilar/' and p.path contains '/index.md' and p.url != '/yazilar/' %}
    {% if p.url == page.url %}
- [{{ p.title }}]({{ site.baseurl }}{{ p.url }})
    {% else %}
- {{ p.title }}
    {% endif %}
  {% endif %}
{% endfor %}
