# Scrum ve Çevik Yazılım Geliştirme

## 1. Scrum Nedir?

**Scrum**, Agile (Çevik) yazılım geliştirme yaklaşımında yaygın olarak kullanılan bir çalışma çerçevesidir.

Scrum'da büyük bir proje tek seferde tamamlanmaya çalışılmaz. Proje daha küçük parçalara bölünür ve bu parçalar **Sprint** adı verilen kısa zaman aralıklarında geliştirilir.

Genellikle bir Sprint:

* 1 hafta
* 2 hafta
* 3 hafta
* En fazla 4 hafta

sürebilir.

Her Sprint'in sonunda çalışır durumda bir ürün parçasının ortaya çıkarılması hedeflenir.

---

# 2. Scrum'ın Temel Akışı

Örneğin bir **yemek sipariş uygulaması** geliştirdiğimizi düşünelim.

Ana hedefimiz:

> Kullanıcıların restoranlardan yemek sipariş edebildiği bir uygulama geliştirmek.

Bu büyük hedef, daha küçük gereksinimlere ayrılır.

Örneğin:

* Kullanıcı kayıt olabilmeli.
* Kullanıcı giriş yapabilmeli.
* Restoranları listeleyebilmeli.
* Ürünleri sepete ekleyebilmeli.
* Ödeme yapabilmeli.
* Sipariş durumunu takip edebilmeli.

Bu gereksinimler **User Story (Kullanıcı Hikâyesi)** şeklinde yazılabilir.

Örneğin:

> "Bir müşteri olarak, sepetime ürün eklemek istiyorum, böylece satın almadan önce ürünlerimi kontrol edebilirim."

---

# 3. Product Backlog

**Product Backlog**, ürünle ilgili yapılması planlanan tüm gereksinimlerin bulunduğu listedir.

Başka bir ifadeyle:

> Product Backlog = Ürün için yapılması gereken işlerin genel listesi

Örneğin:

* Kullanıcı kayıt
* Login
* Şifre sıfırlama
* Restoran listeleme
* Ürün arama
* Sepet
* Ödeme
* Sipariş takibi
* Bildirimler

gibi birçok iş Product Backlog'da bulunabilir.

Product Backlog yalnızca bir Sprint'i değil, ürünün gelecekte yapılması planlanan çalışmalarını da kapsayabilir.

---

# 4. Sprint Backlog

Product Backlog'daki bütün işleri aynı anda yapmaya çalışmayız.

Takım, yaklaşan Sprint içerisinde tamamlanabilecek işleri seçer.

Seçilen bu işler:

**Sprint Backlog**

olarak adlandırılır.

Örneğin Product Backlog'da 50 User Story olduğunu düşünelim.

İki haftalık Sprint için ekip şu 5 işi seçebilir:

1. Kullanıcı kayıt
2. Login
3. Şifre sıfırlama
4. Profil görüntüleme
5. Profil güncelleme

Bu işler Sprint boyunca geliştirilir, test edilir ve mümkünse Sprint sonunda tamamlanır.

---

# 5. Scrum'da Sprint Süreci

Bir Sprint sırasında ekip genel olarak şu faaliyetleri gerçekleştirir:

**Requirement → Planning → Design → Development → Testing → Delivery**

Yani:

1. Gereksinimler incelenir.
2. İşlerin yapılması planlanır.
3. Tasarım oluşturulur.
4. Kod geliştirilir.
5. Testler gerçekleştirilir.
6. Çalışan ürün parçası teslim edilir.

Burada önemli nokta:

> Test, geliştirme bittikten sonra yapılan tek bir aşama değildir.

Test uzmanı Sprint boyunca gereksinimleri inceleyebilir, test senaryolarını hazırlayabilir, geliştirme tamamlandıkça testleri gerçekleştirebilir ve hataları takip edebilir.

---

# 6. Daily Stand-up

Scrum'da ekip genellikle her gün kısa bir toplantı yapar.

Buna:

**Daily Stand-up / Daily Scrum**

denir.

Toplantıda temel olarak şu konular konuşulur:

### Dün ne yaptım?

Örneğin:

> Login test senaryolarını hazırladım.

### Bugün ne yapacağım?

> Login fonksiyonunun testlerine başlayacağım.

### Herhangi bir engelim var mı?

Örneğin:

> Test ortamı çalışmadığı için testlere devam edemiyorum.

Bu toplantının amacı uzun toplantılar yapmak değil, ekibin ilerleyişini ve karşılaşılan engelleri hızlı şekilde görünür hale getirmektir.

---

# 7. Scrum'daki Temel Roller

Scrum'da önemli rollerden bazıları:

## Product Owner (Ürün Sahibi)

Product Owner:

* Ürün gereksinimlerinin yönetilmesinde rol alır.
* User Story'lerin oluşturulması ve önceliklendirilmesinden sorumludur.
* Ürünün ihtiyaçlarını temsil eder.
* Ekibin gereksinimlerle ilgili sorularını yanıtlamaya yardımcı olur.
* Product Backlog'un yönetilmesinde önemli rol oynar.

Test uzmanı açısından Product Owner önemli bir iletişim noktasıdır.

Örneğin gereksinim net değilse tester şu soruyu sorabilir:

> "Bu durumda sistemden beklenen davranış nedir?"

---

## Scrum Master

Scrum Master, Scrum sürecinin doğru şekilde uygulanmasına yardımcı olur.

Görevleri arasında:

* Scrum etkinliklerinin yürütülmesine yardımcı olmak
* Ekibin karşılaştığı engellerin çözülmesini kolaylaştırmak
* Scrum prensiplerinin uygulanmasını desteklemek
* Takımın verimli çalışmasını sağlamak

bulunur.

Önemli:

> Scrum Master klasik anlamda proje yöneticisi olmak zorunda değildir.

Scrum Master'ın temel rolü, Scrum'ın doğru uygulanmasını kolaylaştırmaktır.

---

# 8. Sequential ve Agile Yaklaşım Arasındaki Fark

Geleneksel sıralı geliştirme yaklaşımında genellikle:

**Gereksinimler → Zaman → Kaynak → Bütçe**

başlangıçta daha fazla netleştirilmeye çalışılır.

Örneğin:

> "Gereksinimler belli. Proje 6 ay sürecek. 10 kişilik ekip gerekiyor ve bütçe 1 milyon dolar."

Agile yaklaşımda ise özellikle belirsizliğin yüksek olduğu projelerde daha esnek bir yaklaşım benimsenir.

Örneğin:

> "İki haftalık Sprint içinde hangi işleri tamamlayabiliriz?"

Burada zaman ve ekip kapasitesi daha sabitken, yapılacak işlerin kapsamı önceliklendirilerek değişebilir.

Basit şekilde:

**Sequential:**

> Gereksinimleri belirle → zaman/kaynak/bütçeyi tahmin et.

**Agile:**

> Zaman ve ekip kapasitesini belirle → bu kapasite içerisinde en değerli işleri seç.

---

# 9. Agile'da Neden Küçük Parçalarla İlerlenir?

Çünkü projenin başlangıcında belirsizlik yüksektir.

Başlangıçta şunları tam olarak bilemeyebiliriz:

* Kullanıcı ürünü gerçekten isteyecek mi?
* Gereksinimler doğru mu?
* Teknik çözüm doğru mu?
* Müşteri üründen memnun kalacak mı?
* Hangi özellikler daha önemli?
* Projenin hangi riskleri ortaya çıkacak?

Bu nedenle bütün yatırımı başlangıçta yapmak riskli olabilir.

Bunun yerine:

**Küçük bir ürün → Kullanıcı geri bildirimi → Öğrenme → Geliştirme → Daha fazla yatırım**

şeklinde ilerlenebilir.

---

# 10. MVP ve Agile Yaklaşımı

Özellikle yeni ve belirsiz projelerde **MVP (Minimum Viable Product)** yaklaşımı kullanılabilir.

MVP:

> Ürünün temel fikrini test etmeye yetecek minimum kullanılabilir ürün.

Örneğin yeni bir yapay zekâ uygulaması geliştirdiğimizi düşünelim.

Başlangıçta:

* Çok büyük bir sistem kurmak
* Kendi yapay zekâ modelimizi geliştirmek
* Büyük altyapı yatırımı yapmak

yerine mevcut API'lerden yararlanarak küçük bir prototip/MVP oluşturabiliriz.

Sonra kullanıcıların tepkisini gözlemleriz.

Eğer:

* Kullanıcılar ürünü seviyorsa,
* Talep varsa,
* İş modeli çalışıyorsa,

daha fazla yatırım yapılabilir.

Bu yaklaşım Agile düşünceyle uyumludur.

---

# 11. Belirsizlik Konisi (Cone of Uncertainty)

Projelerin başlangıcında belirsizlik genellikle daha yüksektir.

Proje ilerledikçe:

* Gereksinimler daha iyi anlaşılır.
* Teknik problemler ortaya çıkar ve çözülür.
* Kullanıcı geri bildirimleri alınır.
* Riskler daha görünür hale gelir.
* Tahminler daha doğru hale gelir.

Bu nedenle başlangıçta çok kesin tahminler yapmak risklidir.

Basit olarak:

**Projenin başı → yüksek belirsizlik**

**Proje ilerledikçe → belirsizlik azalır**

Bu nedenle Agile yaklaşımlar küçük adımlarla ilerleyerek belirsizliği azaltmaya çalışır.

---

# 12. Risk ve Yatırım İlişkisi

Belirsizlik yüksekken büyük yatırımlar yapmak riskli olabilir.

Örneğin:

> Bir şirket yeni bir yapay zekâ ürünü geliştirmek istiyor.

İlk günden milyonlarca lira harcayıp büyük bir altyapı kurmak yerine:

1. Küçük bir prototip oluşturabilir.
2. MVP geliştirebilir.
3. Kullanıcı geri bildirimlerini toplayabilir.
4. Ürünün gerçekten talep görüp görmediğini ölçebilir.
5. Başarılıysa yatırımı artırabilir.

Bu yaklaşım:

**Build → Measure → Learn**

mantığıyla da ilişkilendirilebilir.

---

# 13. Test Uzmanı Açısından Scrum

Bir test uzmanı için Scrum'ın en önemli taraflarından biri şudur:

> Tester Sprint'in sonunda sadece ürünü kontrol eden kişi değildir.

Tester Sprint boyunca sürece dahil olabilir.

### Sprint öncesinde

* User Story'leri inceler.
* Gereksinimlerin test edilebilir olup olmadığını değerlendirir.
* Belirsiz noktaları sorar.
* Acceptance Criteria'ları inceler.
* Test senaryolarını planlar.

### Sprint sırasında

* Test case'leri oluşturur.
* Fonksiyonel testler yapar.
* API testleri gerçekleştirir.
* SQL ile veri doğrulaması yapabilir.
* Hataları raporlar.
* Developer tarafından düzeltilen hataları retest eder.
* Gerekirse regression test yapar.

### Sprint sonunda

* Tamamlanan özellikleri doğrular.
* Test sonuçlarını değerlendirir.
* Açık kalan bug'ları takip eder.
* Sprint Review ve Retrospective süreçlerine katkıda bulunabilir.

---

# 14. Tester'ın User Story'ye Bakışı

Bir tester User Story'yi yalnızca:

> "Ne geliştirilecek?"

diye okumaz.

Aynı zamanda:

> "Bunu nasıl test edebilirim?"

diye düşünür.

Örneğin:

**User Story:**

> "Bir kullanıcı olarak hesabıma giriş yapmak istiyorum."

Tester şu soruları sorabilir:

* Doğru kullanıcı adı ve şifre ile ne olmalı?
* Yanlış şifre ile ne olmalı?
* Boş kullanıcı adı ile ne olmalı?
* Boş şifre ile ne olmalı?
* Hesabı kilitli kullanıcı ne yapmalı?
* Çok fazla başarısız girişte ne olmalı?
* Şifre büyük/küçük harfe duyarlı mı?
* Mobil ve web'de davranış aynı mı?
* API üzerinden giriş yapıldığında ne olmalı?

Böylece tester gereksinimi farklı açılardan inceleyerek **pozitif, negatif ve edge case** senaryolarını oluşturabilir.

---

# 15. Scrum'da Test Açısından Önemli Kavramlar

| Kavram              | Açıklama                                                       |
| ------------------- | -------------------------------------------------------------- |
| Scrum               | Agile çalışma çerçevesi                                        |
| Sprint              | Kısa ve zaman kutulu geliştirme dönemi                         |
| Product Backlog     | Ürün için yapılması planlanan işlerin listesi                  |
| Sprint Backlog      | Mevcut Sprint'te yapılacak seçilmiş işler                      |
| User Story          | Kullanıcı ihtiyacını anlatan gereksinim                        |
| Product Owner       | Ürün ve gereksinimlerin yönetiminde önemli rol                 |
| Scrum Master        | Scrum sürecinin uygulanmasını kolaylaştırır                    |
| Daily Scrum         | Günlük kısa ekip toplantısı                                    |
| MVP                 | Ürünün temel fikrini test eden minimum kullanılabilir sürüm    |
| Acceptance Criteria | Bir User Story'nin kabul edilmesi için gereken koşullar        |
| Retest              | Düzeltilen hatanın tekrar test edilmesi                        |
| Regression Test     | Değişikliklerin mevcut özellikleri bozup bozmadığının kontrolü |

---

# 16. Yazılım Test Uzmanı İçin En Önemli Çıkarım

Scrum'ı öğrenirken sadece rollerin ve toplantıların isimlerini ezberlemek yeterli değildir.

Bir tester olarak şu mantığı anlamak gerekir:

> **Gereksinim → User Story → Acceptance Criteria → Test Senaryosu → Test Case → Test → Bug → Retest → Regression → Delivery**

Scrum ortamında tester, geliştirme sürecinin sonunda devreye giren kişi değil, **Sprint boyunca kaliteye katkı sağlayan ekip üyesidir.**

---

## Kısa Ezber

**Scrum:**

> Büyük işi küçük Sprint'lere böl.

**Product Backlog:**

> Yapılması gereken tüm işler.

**Sprint Backlog:**

> Bu Sprint'te yapacağımız işler.

**Daily Scrum:**

> Dün ne yaptım? Bugün ne yapacağım? Engelim var mı?

**Product Owner:**

> Ürün ve gereksinimlerin önceliklendirilmesine odaklanır.

**Scrum Master:**

> Scrum sürecinin sağlıklı işlemesini kolaylaştırır.

**Agile:**

> Küçük parçalarla ilerle, geri bildirim al, öğren ve adapte ol.

**Tester:**

> Gereksinimden itibaren kaliteye katkı sağlar.

**Belirsizlik:**

> Başlangıçta yüksek → proje ilerledikçe azalır.

**MVP:**

> Büyük yatırım yapmadan fikri küçük ölçekte test et.
