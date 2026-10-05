# Yazılım Geliştirme Ekibindeki Roller

## 1. Neden Rolleri Bilmek Önemlidir?

Bir yazılım test uzmanı yalnızca test ekibiyle çalışmaz.

Yazılım geliştirme sürecinde;

* Product Owner
* Business Analyst
* Project Manager
* UI/UX Designer
* Front-end Developer
* Back-end Developer
* Mobile Developer
* Scrum Master

gibi farklı rollerle iletişim kurar.

Tester'ın görevi yalnızca hata bulmak değildir.

Tester aynı zamanda:

> **Doğru gereksinimi anlamalı, doğru kişiye doğru bilgiyi iletmeli ve bulunan problemin hangi ekip tarafından ele alınması gerektiğini anlayabilmelidir.**

Bu nedenle test uzmanının diğer rollerin görevlerini temel düzeyde bilmesi büyük avantaj sağlar.

---

# 2. T-Şekilli Profesyonel (T-Shaped Professional)

**T-shaped professional**, bir kişinin bir alanda derin uzmanlığa sahip olurken diğer alanlarda da geniş bir bilgiye sahip olmasıdır.

Örneğin bir yazılım test uzmanı:

**Derinlik:**

* Manual Testing
* Test Case
* Bug Reporting
* API Testing
* SQL

konularında uzmanlaşabilir.

**Genişlik:**

* Business Analysis
* Product Management
* UI/UX
* Development
* Agile/Scrum
* DevOps

konularında temel bilgi sahibi olabilir.

Tester'ın geliştirici olması gerekmez.

Ancak geliştiricinin ne yaptığını, API'nin ne olduğunu, gereksinimin nasıl oluşturulduğunu ve ürün sahibinin neye karar verdiğini anlaması işini kolaylaştırır.

Bu nedenle:

> **Derin uzmanlık + geniş perspektif = T-shaped professional**

---

# 3. Product Owner (Ürün Sahibi)

Product Owner, ürünün iş değerine ve müşteri ihtiyaçlarına odaklanan roldür.

Temel sorularından biri:

> "Ne geliştirmeliyiz?"

Product Owner'ın sorumlulukları arasında:

* Ürün vizyonunu anlamak
* Gereksinimleri yönetmek
* User Story'lerin oluşturulmasına katkı sağlamak
* Önceliklendirme yapmak
* Product Backlog'u yönetmek
* İş değerini gözetmek

bulunur.

## Tester ile ilişkisi

Tester, Product Owner ile gereksinimleri ve beklenen davranışı anlamak için iletişim kurabilir.

Örneğin:

> "Kullanıcı iki farklı indirim kuponunu aynı anda kullanabilir mi?"

> "Bu durumda beklenen sonuç nedir?"

> "Bu özellik zorunlu mu?"

Tester ayrıca Product Owner tarafından oluşturulan User Story'leri inceleyerek belirsizlikleri ve eksikleri tespit edebilir.

---

# 4. User Story

User Story, kullanıcının ihtiyacını ifade eden gereksinim biçimlerinden biridir.

Yaygın format:

> **Bir [kullanıcı] olarak, [bir işlem] yapmak istiyorum, böylece [bir fayda] elde edebilirim.**

Örneğin:

> Bir müşteri olarak, kredi kartımı kaydetmek istiyorum, böylece sonraki alışverişlerimde daha hızlı ödeme yapabilirim.

Tester bu User Story'yi okurken sadece "ne geliştirilecek?" diye düşünmez.

Aynı zamanda:

* Nasıl test edeceğim?
* Beklenen sonuç nedir?
* Hangi koşullarda çalışmalı?
* Hangi koşullarda çalışmamalı?
* Edge case'ler neler?
* Kabul kriterleri yeterli mi?

sorularını sorar.

---

# 5. INVEST Tekniği

User Story'lerin kalitesini değerlendirmek için **INVEST** prensipleri kullanılabilir.

| Harf | Anlamı      | Açıklama                                                    |
| ---- | ----------- | ----------------------------------------------------------- |
| I    | Independent | Hikâye mümkün olduğunca diğer hikâyelerden bağımsız olmalı  |
| N    | Negotiable  | Nasıl geliştirileceğini değil, neyin yapılacağını anlatmalı |
| V    | Valuable    | Kullanıcı veya iş için değer sağlamalı                      |
| E    | Estimable   | Eforu tahmin edilebilir olmalı                              |
| S    | Small       | Sprint içerisinde yönetilebilir büyüklükte olmalı           |
| T    | Testable    | Test edilebilir olmalı                                      |

### Tester açısından özellikle önemli:

**Testable**

Bir User Story'nin test edilebilir olması gerekir.

Örneğin:

> "Uygulama hızlı olmalıdır."

test açısından yeterince açık değildir.

Bunun yerine:

> "Ödeme onay ekranı normal yük koşullarında 3 saniye içerisinde görüntülenmelidir."

daha ölçülebilir ve test edilebilir bir gereksinimdir.

---

# 6. Business Analyst (İş Analisti)

Business Analyst, iş ihtiyaçları ile teknik ekip arasında önemli bir köprü görevi görür.

Temel görevi:

> İş ihtiyacını anlayıp bunu geliştirme ekibinin kullanabileceği gereksinimlere dönüştürmek.

Business Analyst:

* Gereksinimleri toplar.
* Paydaşlarla iletişim kurar.
* Gereksinimleri analiz eder.
* Detaylı gereksinimler oluşturur.
* Kabul kriterlerinin belirlenmesine katkı sağlar.
* İş ihtiyaçlarını geliştirme ekibine aktarır.

Bazı şirketlerde Product Owner ve Business Analyst görevleri aynı kişi tarafından yürütülebilir.

Ancak:

> **Product Owner ve Business Analyst aynı rol değildir.**

---

# 7. Tester – Business Analyst İlişkisi

Tester, Business Analyst tarafından oluşturulan gereksinimleri dikkatli şekilde incelemelidir.

Örneğin:

> "Müşteri indirim kullanabilir."

Tester burada durmaz.

Şunları sorar:

* Hangi müşteriler?
* Hangi ürünlerde?
* İndirim oranı nedir?
* Birden fazla indirim kullanılabilir mi?
* İndirimler birbiriyle birleşebilir mi?
* İndirim süresi geçmişse ne olur?
* Minimum sepet tutarı var mı?
* İndirim uygulanamazsa kullanıcıya ne gösterilecek?

Bu yaklaşım sayesinde hataların geliştirme başlamadan önce yakalanması mümkün olur.

Bu da **Early Testing / Shift Left** yaklaşımıyla ilişkilidir.

---

# 8. Functional ve Non-Functional Requirements

Gereksinimler genel olarak iki önemli gruba ayrılabilir.

## Functional Requirements

Sistemin **ne yapması gerektiğini** ifade eder.

Örneğin:

* Kullanıcı kayıt olabilmeli.
* Kullanıcı giriş yapabilmeli.
* Kullanıcı ürün ekleyebilmeli.
* Kullanıcı ödeme yapabilmeli.
* Sistem kart numarasını doğrulamalı.

---

## Non-Functional Requirements

Sistemin bir işlevi **hangi kalite özellikleriyle** gerçekleştirmesi gerektiğini ifade eder.

Örneğin:

* Performans
* Güvenlik
* Kullanılabilirlik
* Erişilebilirlik
* Ölçeklenebilirlik
* Güvenilirlik

Örnek:

> "Ödeme onay ekranı normal yük koşullarında 3 saniye içerisinde açılmalıdır."

Burada yalnızca "ekran açılmalı" denmiyor.

**Ne kadar sürede açılacağı** da belirtiliyor.

---

# 9. Non-Functional Testing

Non-functional gereksinimler de test edilmelidir.

Örneğin:

### Performance Testing

Sistem belirli yük altında kabul edilebilir performans gösteriyor mu?

### Security Testing

Yetkisiz kullanıcı verilere erişebiliyor mu?

### Usability Testing

Sistem kullanıcı tarafından kolay kullanılabiliyor mu?

### Accessibility Testing

Farklı kullanıcı ihtiyaçları için erişilebilir mi?

Bu testlerin tamamı klasik manuel fonksiyonel testlerle sınırlı değildir.

Bazıları için özel araçlar, teknikler ve test ortamları gerekir.

---

# 10. MoSCoW Önceliklendirme

Gereksinimleri önceliklendirmek için **MoSCoW** yöntemi kullanılabilir.

### M — Must Have

Olmazsa olmaz gereksinimler.

Ürünün çalışması için gereklidir.

Örneğin:

> E-ticaret uygulamasında ödeme yapabilme.

### S — Should Have

Önemlidir ancak gerektiğinde ertelenebilir.

### C — Could Have

Olması güzel olan ancak zorunlu olmayan özellikler.

### W — Won't Have

Mevcut kapsamda yapılmayacak özellikler.

Örneğin:

> Uygulamanın ilk sürümünde telefon numarasıyla kayıt olmayacak, yalnızca e-posta ile kayıt yapılacak.

---

# 11. MoSCoW ve Tester İlişkisi

Gereksinimin önceliği test ve bug yönetimini de etkileyebilir.

Örneğin:

**Must Have** bir ödeme özelliğinde kritik bir hata varsa ürünün yayınlanması engellenebilir.

Ancak:

**Could Have** kategorisindeki küçük bir görsel problem ürünün yayınlanmasını mutlaka engellemeyebilir.

Bu nedenle tester yalnızca:

> "Bug var."

dememelidir.

Aynı zamanda:

> "Bu bug'ın ürün ve kullanıcı üzerindeki etkisi nedir?"

diye düşünmelidir.

---

# 12. Project Manager (Proje Yöneticisi)

Project Manager, projenin planlanması ve takip edilmesiyle ilgilenir.

Temel konuları:

* Zaman
* Kapsam
* Kaynak
* Bütçe
* Risk
* İlerleme
* Proje planı

olabilir.

Project Manager'ın görevi doğrudan tester'ı yönetmek olmak zorunda değildir.

---

# 13. Tester – Project Manager İlişkisi

Test faaliyetleri proje planından bağımsız değildir.

Örneğin:

> Ürünün 30 Haziran'da canlıya alınması planlanıyorsa test faaliyetlerinin de bu tarihe göre planlanması gerekir.

Tester:

* Test ilerlemesini raporlayabilir.
* Test süresini planlayabilir.
* Test risklerini bildirebilir.
* Test için gereken kaynakları belirtebilir.
* Gecikmeleri paylaşabilir.
* Kritik bug'ları raporlayabilir.

### Risk ve Test

Risk yüksekse genellikle daha fazla test ve daha dikkatli doğrulama gerekir.

Örneğin:

Bir ödeme sistemindeki hata ile küçük bir renk probleminin riski aynı değildir.

---

# 14. Gantt Chart

Proje planlamasında **Gantt Chart** kullanılabilir.

Gantt Chart, görevlerin:

* Ne zaman başlayacağını
* Ne zaman biteceğini
* Ne kadar süreceğini
* Birbirleriyle olan bağımlılıklarını

gösterebilir.

Örneğin:

**Requirements → Design → Development → Test → Deployment**

şeklinde bir bağımlılık bulunabilir.

Tester, kendi test faaliyetlerini bu plana göre organize eder.

---

# 15. UI/UX Designer

UI/UX Designer:

* Kullanıcı arayüzünü tasarlar.
* Kullanıcı deneyimini düşünür.
* Ekranları tasarlar.
* Kullanılabilirliği geliştirir.
* Wireframe ve yüksek detaylı tasarımlar oluşturabilir.

---

# 16. Wireframe ve Mockup/Figma Tasarımı

Bu iki kavramı ayırmak önemlidir.

## Wireframe

Wireframe daha çok:

> "Bu ekranda hangi öğeler bulunacak?"

sorusuna odaklanır.

Örneğin ödeme ekranında:

* Kart numarası
* Son kullanma tarihi
* CVV
* Kart sahibi adı
* Ödeme butonu

bulunacağını gösterir.

Renk, yazı tipi ve görsel ayrıntılar ön planda değildir.

---

## Mockup / High-Fidelity Design

Daha gerçekçi ve görsel açıdan detaylı tasarımdır.

Örneğin:

* Renkler
* Fontlar
* Boşluklar
* Buton tasarımları
* Hizalamalar
* Görsel öğeler

gibi detayları içerir.

Figma gibi araçlarda hazırlanabilir.

---

# 17. Tester – UI/UX Designer İlişkisi

Tester tasarlanmış ekranı inceleyebilir.

### Wireframe testinde:

* Gerekli alanlar var mı?
* Kart numarası alanı var mı?
* Ödeme butonu var mı?
* Sipariş özeti bulunuyor mu?

### High-Fidelity Design testinde:

* Renkler doğru mu?
* Font doğru mu?
* Öğeler doğru hizalanmış mı?
* Tasarım gereksinimle uyumlu mu?
* Responsive davranış uygun mu?
* Erişilebilirlik açısından problem var mı?

Tester böylece tasarım aşamasında da kaliteye katkıda bulunabilir.

---

# 18. Front-End Developer

Front-end developer, kullanıcının gördüğü ve etkileşimde bulunduğu kısmı geliştirir.

Örneğin:

* Web sayfaları
* Butonlar
* Formlar
* Menü
* Navigasyon
* UI bileşenleri

front-end kapsamındadır.

Kullanılan teknolojilere örnek:

* HTML
* CSS
* JavaScript
* Front-end framework'leri

---

# 19. Tester – Front-End Developer İlişkisi

Tester'ın bulduğu bazı hatalar front-end geliştiriciye atanabilir.

Örneğin:

* Yanlış hizalama
* Responsive tasarım problemi
* UI problemi
* Yanlış navigasyon
* Çalışmayan buton
* Client-side validation problemi
* Yanlış görüntülenen içerik

Örneğin:

> "Kaydol" butonu tasarımda sağ tarafta olması gerekirken başka bir yerde görüntüleniyor.

Bu tür bir problem front-end ile ilişkili olabilir.

Ancak tester sadece görüntüye bakarak hatanın kesin olarak front-end'e ait olduğunu varsaymamalıdır.

Problemin kaynağını anlamak için gerekirse:

**UI → API → Backend → Database**

akışı incelenmelidir.

---

# 20. Back-End Developer

Back-end developer, uygulamanın arka plandaki işleyişinden sorumludur.

Örneğin:

* Business Logic
* Server-side işlemler
* API'ler
* Veri işleme
* Yetkilendirme
* Veritabanı işlemleri

gibi konularla ilgilenir.

Kullanıcı genellikle back-end'i doğrudan görmez.

---

# 21. Tester – Back-End Developer İlişkisi

Back-end kaynaklı problemlere örnek:

* Yanlış business logic
* Yanlış hesaplama
* API'nin yanlış cevap vermesi
* Yanlış HTTP status code
* Yetkilendirme problemi
* Veri işleme problemi
* Güvenlik problemi
* Sipariş toplamının yanlış hesaplanması

Örneğin:

> Kullanıcı iki ürünü sepete ekliyor fakat API toplam fiyatı yanlış döndürüyor.

Bu durumda problem yalnızca UI'da değildir.

Tester API'yi inceleyerek problemin back-end tarafında olduğunu gösterebilir.

---

# 22. API ve Tester

Front-end ile back-end arasındaki iletişimde API'ler önemli rol oynar.

Örneğin:

**Frontend → API → Backend → Database**

Bir ödeme işleminde:

1. Kullanıcı "Öde" butonuna basar.
2. Front-end ödeme bilgilerini API'ye gönderir.
3. Back-end bilgileri doğrular.
4. Ödeme sistemiyle iletişim kurulur.
5. İşlem veritabanına kaydedilir.
6. Sonuç front-end'e gönderilir.
7. Kullanıcı başarılı/başarısız sonucunu görür.

Tester bu akışı anlarsa hatanın kaynağını daha doğru analiz edebilir.

---

# 23. HTTP Methods

API testlerinde sık karşılaşılan HTTP method'ları:

* **GET** → Veri alma
* **POST** → Yeni veri/işlem oluşturma
* **PUT** → Veriyi güncelleme
* **DELETE** → Veri silme

API testing konusunda Postman gibi araçlar kullanılabilir.

---

# 24. Mobile Developer

Mobile Developer, mobil cihazlarda çalışan uygulamaları geliştirir.

Örneğin:

* Android
* iOS
* Tablet
* Bazı durumlarda wearable cihazlar

için uygulamalar geliştirebilir.

Mobil geliştirici:

* Android Developer
* iOS Developer
* Cross-platform Developer

şeklinde farklı uzmanlıklara sahip olabilir.

---

# 25. Tester – Mobile Developer İlişkisi

Android ve iOS için ayrı kod tabanları varsa:

> Android'de bulunan bir bug'ın iOS'ta da bulunacağı garanti değildir.

Bu nedenle aynı fonksiyonun farklı platformlarda test edilmesi gerekir.

Örneğin:

**Test Senaryosu:**

> Geçerli kullanıcı bilgileriyle giriş yap.

Bu senaryo:

* Android
* iOS

üzerinde ayrı ayrı doğrulanabilir.

Cross-platform geliştirmede ise test stratejisi kullanılan teknolojiye ve uygulamanın yapısına göre farklılaşabilir.

---

# 26. Mobil Testte Dikkat Edilecekler

Tester mobil uygulamalarda yalnızca fonksiyonları değil;

* Farklı ekran boyutlarını
* Farklı işletim sistemlerini
* Farklı cihazları
* Orientation değişikliklerini
* Network koşullarını
* Uygulama izinlerini
* Bildirimleri
* Performansı
* Responsive davranışı

da dikkate alabilir.

---

# 27. Scrum Master

Scrum Master, Scrum framework'ünün uygulanmasını kolaylaştıran kişidir.

Scrum Master:

* Scrum etkinliklerini kolaylaştırır.
* Takımın önündeki engellerin kaldırılmasına yardımcı olur.
* Takımın Scrum prensiplerine uygun çalışmasını destekler.
* İletişimi kolaylaştırır.
* Sürecin iyileştirilmesini destekler.

Önemli:

> **Scrum Master klasik anlamda takımın yöneticisi değildir.**

Ekibe görev dağıtan bir yönetici olmak zorunda değildir.

Daha çok:

> **Facilitator + Coach**

rolündedir.

---

# 28. Tester – Scrum Master İlişkisi

Tester'ın test yapmasını engelleyen bir problem varsa Scrum Master yardımcı olabilir.

Örneğin:

> Test ortamı çalışmıyor.

> Gerekli test verileri hazır değil.

> Başka bir ekip nedeniyle test faaliyetleri başlayamıyor.

> Developer ile bug'ın sorumluluğu konusunda anlaşmazlık yaşanıyor.

Tester bu engelleri Scrum Master'a iletebilir.

Scrum Master sorunu kendisi teknik olarak çözmek zorunda değildir.

Gerekli kişilerle iletişim kurarak problemin çözülmesini kolaylaştırır.

---

# 29. Scrum Board

Scrum süreçlerinin takibinde bir Scrum Board kullanılabilir.

Örneğin:

**To Do → In Progress → Review → Testing → Done**

Bir User Story veya görev süreç ilerledikçe bu kolonlar arasında hareket eder.

Tester açısından özellikle:

**Testing**

aşaması önemlidir.

Ancak modern Agile ekiplerde test yalnızca tek bir kolon olarak değil, işin tamamlanmasının bir parçası olarak ele alınabilir.

---

# 30. Burndown Chart

**Burndown Chart**, Sprint içerisinde kalan iş miktarının zaman içerisinde nasıl azaldığını göstermeye yardımcı olur.

Örneğin iki haftalık Sprint'te:

* Başlangıçta çok sayıda iş vardır.
* Günler ilerledikçe tamamlanan işler artar.
* Kalan iş miktarı azalır.

Tester açısından bu grafik Sprint'in hedeflerine doğru ilerleyip ilerlemediğini anlamaya yardımcı olabilir.

---

# 31. Roller Arası İletişim

Bir yazılım test uzmanının ekip içerisindeki iletişimini şu şekilde düşünebiliriz:

```text
                    Product Owner
                         ↕
                  Business Analyst
                         ↕
UI/UX Designer ↔ TESTER ↔ Developers
                         ↕
                   Scrum Master
                         ↕
                  Project Manager
```

Ancak gerçek projelerde iletişim yalnızca bu şekilde doğrusal değildir.

Tester gerektiğinde farklı rollerle doğrudan iletişim kurabilir.

---

# 32. Tester'ın Asıl Değeri

İyi bir tester:

> "Ben sadece test yapıyorum."

diyen kişi değildir.

İyi bir tester:

* Gereksinimi sorgular.
* Belirsizlikleri bulur.
* Riskleri değerlendirir.
* Kullanıcı perspektifini düşünür.
* Tasarımı inceler.
* API'yi anlayabilir.
* Veritabanını gerektiğinde kontrol eder.
* Hatanın kaynağını araştırır.
* Doğru kişiye doğru bug'ı atar.
* Geliştiriciyle teknik iletişim kurabilir.
* Product Owner/Business Analyst ile iş gereksinimini konuşabilir.

Bu nedenle tester'ın teknik bilgi kadar **iletişim ve analiz becerisi** de önemlidir.

---

# 33. Test Uzmanı İçin Rol → Çıktı → İlişki Tablosu

| Rol                 | Temel Çıktı                              | Tester'ın İlişkisi                              |
| ------------------- | ---------------------------------------- | ----------------------------------------------- |
| Product Owner       | Product Backlog, User Story              | Gereksinimleri ve öncelikleri anlamak           |
| Business Analyst    | Gereksinimler, Acceptance Criteria       | Belirsizlikleri ve eksikleri bulmak             |
| Project Manager     | Proje planı, zamanlama                   | Test faaliyetlerini plana göre yürütmek         |
| UI/UX Designer      | Wireframe, Mockup, Figma tasarımı        | Tasarım ve kullanılabilirliği doğrulamak        |
| Front-end Developer | Kullanıcı arayüzü                        | UI ve client-side problemleri test etmek        |
| Back-end Developer  | API, business logic, veri işlemleri      | API, iş kuralları ve veri akışını test etmek    |
| Mobile Developer    | Android/iOS uygulaması                   | Mobil platformlarda fonksiyonları doğrulamak    |
| Scrum Master        | Scrum Board, süreç takibi, kolaylaştırma | Test engellerini ve süreç problemlerini iletmek |

---

# 34. İş Görüşmesi İçin Kritik Bakış Açısı

Bir görüşmede:

> "Front-end developer ne yapar?"

sorusuna yalnızca:

> "Kullanıcı arayüzünü geliştirir."

demek yeterli olabilir ama daha güçlü cevap şudur:

> "Front-end developer kullanıcıların gördüğü ve etkileşimde bulunduğu kısmı geliştirir. Tester olarak UI, navigasyon, client-side validation ve responsive davranış gibi konuları test ederim. Ancak bulduğum problemin gerçekten front-end kaynaklı olup olmadığını anlamak için gerektiğinde API ve back-end akışını da kontrol ederim."

Bu cevap, ezberden daha fazla şey gösterir:

**Test bilgisi + teknik anlayış + problem çözme + ekip iletişimi.**

---

# Kısa Ezber

**Product Owner**
→ Ne yapılmalı?

**Business Analyst**
→ İş ihtiyacı nasıl gereksinime dönüştürülmeli?

**Project Manager**
→ Proje nasıl planlanmalı ve takip edilmeli?

**UI/UX Designer**
→ Kullanıcı ne görecek ve nasıl deneyimleyecek?

**Front-end Developer**
→ Kullanıcı ne görecek ve neyle etkileşecek?

**Back-end Developer**
→ Sistem arka planda nasıl çalışacak?

**Mobile Developer**
→ Uygulama mobil cihazlarda nasıl çalışacak?

**Scrum Master**
→ Ekip Scrum sürecini nasıl daha sağlıklı uygulayacak?

**Tester**
→ Gereksinim doğru mu, ürün beklenen şekilde çalışıyor mu ve kalite açısından risk var mı?

---

## En önemli cümle

> **Tester'ın görevi yalnızca bug bulmak değil; gereksinimden ürüne kadar kaliteyi sorgulamaktır.**

Bu nedenle yazılım geliştirme ekibindeki diğer rollerin görevlerini anlamak, test uzmanının hem **daha iyi test yapmasını** hem de **bug'ı doğru kişiye doğru gerekçeyle aktarabilmesini** sağlar.
