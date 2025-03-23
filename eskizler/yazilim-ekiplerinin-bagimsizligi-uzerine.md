---
title: Yazılım Ekiplerinin Bağımsızlığı Üzerine
---

Her ekip kendi tercihlerini hem teknolojik, hem de tasarımsal açıdan yapabilmek
ister. Bunu sağlamak kolay değildir, korumak hiç kolay değildir. Uzmanlığa göre
belirlenmiş bir takım için bu daha da zordur. Front-end, back-end, mobil gibi.

Neden?

Back-end takımı bir REST standardı belirler ve böyle yazacağız der. Bu standart
aslında front-end ekibine yapılan bir dayatmadır. Uzlaşmalarını isterseniz de
bu pek verimli olmaz. En iyi ihtimalle agree-to-disagree seçeneğinde kalırsınız.
Kimse anlaşamaz demiyorum, ama şirket tarihinize bakarsanız anlaşamadıkları an
anlaşabildiklerinden daha azdır. Örneğin front-end ekibi graph-ql ister,
back-end ise bunu sunmayabilir.

Bu dayatma bağımlı olunan takımdan bağımlı olan takıma doğru olmak zorunda da
değildir. Yani sadece back-end'den front-end'e dayatma olmaz. Uygulama
yazılmıştır, her şey güzel çalışıyordur. Front-end ekibi css yapısını düzenleme
niyetindedir, zorla ikna olduğu servis katmanına hiç dokunası yoktur. Back-end
ekibi ise belki usul değişikliğine (rest -> graphql), büyük ihtimalle de api'da
isimlendirme ya da model değişikliğine gitmek istemektedir. Hatta belki api
çağrılarındaki akışı değiştirmek ister. Front-end ekibi buna vakit ayırmak
istemez, ya da sonra yapacağını söyler ve ya iş yapılmaz ya da back-end ekibi
geriye dönük destek verecek şekilde pozisyon alır ve aylarca bazen de yıllarca
eski api'yi silemez, maintenance maliyeti doğar.

Hem uygulamaların bağımsız release'ler ile ilerleyebilmesi, hem de teknoloji
tercihlerinin bağımsız yapılabilmesi için anahtar soyutlamadır. Burada bir
sürpriz yok. Yalnız front-end back-end'i soyutlarsa, back-end de front-end'i
soyutlarsa, bu iki soyutlama arasındaki bağı kurmak kimin görevidir? Bu işin
doğrusu olmadığı gibi, konu teknik bir konu da değil, politik bir konudur

Front-end ekibi müşteriye daha yakın, son kullanıcıya dokunması sebebi ile iç
politikada daha baskınsa, o iş back-end'e kalır. Back-end maintenance
pozisyonunda, burnundan kıl aldırmayan, o öyle olmaz, bu böyle yapılmaz, onun
için 7 ay çalışmamız gerekir diyen, bakımcı pozisyonunu dayatabilmişse, o iş
front-end'e kalır. Front-end ekibi outsource'sa ya da dışarıdan gelen bir proje
ekibi ise, o iş yine front-end'e kalır. Entegrasyon yapan firma, entegrasyon
yapılan firmaya söz geçirebiliyorsa, finansal olarak vazgeçilemeyecek
pozisyondaysa, bırakın iki soyutlama arasındaki bağı oluşturma sorumluluğunu
o firmaya özel yepyeni api dahi yazdırırlar back-end ekibine.

Bunun ne anlamı var? Herhangi bir ekip bağımsız olmak istiyorsa, bugün yaptığı
tercihlerin kendisini yarın daha az bağlamasını istiyorsa, buna göre pozisyon
almalıdır. Hem politik olarak, hem de, ve çoğunlukla, teknik olarak.

Dış bağımlılıklardan tamamen soyutlanacak şekilde yazılım tasarlamalı, ve bunu
değişimin maliyetini artırmayacak şekilde yapmalıdır. Ayrıca sistemini hem
teknoloji, hem de usul değişikliklerine de hazır tutmalıdır. Ve politik
pozisyonunu iyi görmeli, kendisini muhtemel ek sorumluluklara yine değişim
maliyetini artırmayacak şekilde hazırlamalıdır.
