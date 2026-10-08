# Yazılım Testine Giriş

## 1. Yazılım Testi Nedir?

Yazılım testi, bir yazılımın belirtilen gereksinimleri karşılayıp karşılamadığını değerlendirmek ve kusurları ortaya çıkarmak amacıyla yürütülen sistematik bir süreçtir.

Test süreci yalnızca yazılımı çalıştırmayı değil; gereksinimleri incelemeyi, testleri planlamayı, test senaryoları hazırlamayı, testleri yürütmeyi, sonuçları değerlendirmeyi ve hataları raporlamayı da kapsar.

## 2. Yazılım Testinin Amaçları

* Yazılımdaki kusurları ortaya çıkarmak.
* Gereksinimlerin karşılanıp karşılanmadığını değerlendirmek.
* Yazılımın ve ilgili iş ürünlerinin kalitesi hakkında bilgi sağlamak.
* Paydaşların ürünün risklerini ve mevcut kalite düzeyini anlamasına yardımcı olmak.
* Hataların son kullanıcıya ulaşma olasılığını ve olası maliyetlerini azaltmak.
* Kullanıcı güvenini ve işletmenin itibarını korumaya katkıda bulunmak.

**Önemli:** Yazılım testi, yazılımın hatasız olduğunu kanıtlayamaz. Testler kusurların varlığını gösterebilir; ancak test sırasında kusur bulunmaması, hiç kusur olmadığı anlamına gelmez.

## 3. Kalite Herkesin Sorumluluğudur

Yazılım kalitesi yalnızca test uzmanına bağlı değildir.

* **Test uzmanı:** Testleri planlar, senaryolar hazırlar, testleri yürütür ve kusurları raporlar.
* **Geliştirici:** Kodun doğruluğunu değerlendirir, birim testlerini yapar ve kusurları düzeltir.
* **Ürün sahibi ve iş analisti:** Gereksinimlerin ve kabul kriterlerinin açıklığa kavuşturulmasına katkıda bulunur.
* **Operasyon ekibi:** Üretim ortamını izler ve karşılaşılan sorunları bildirir.
* **Kullanıcılar:** Beta testleri ve geri bildirimler aracılığıyla sorunların ortaya çıkarılmasına katkı sağlayabilir.

Kalite, ekip üyelerinin birlikte çalışmasıyla geliştirilir.

## 4. Yazılım Testi Hakkındaki Yaygın Yanlış Anlamalar

### Yanlış 1: Test etmek sadece tıklamaktır.

**Doğrusu:** Test; planlama, analiz, tasarım, uygulama, sonuç değerlendirme ve raporlama gibi faaliyetleri içeren sistematik bir süreçtir.

### Yanlış 2: Bütün testleri yalnızca test uzmanı yapar.

**Doğrusu:** Geliştiriciler birim testleri yapar; test uzmanları farklı test seviyelerinde ve türlerinde görev alır. Diğer ekip üyeleri de kaliteye katkıda bulunur.

### Yanlış 3: Geliştiriciler birim testlerini yaptıysa başka teste gerek yoktur.

**Doğrusu:** Bileşenler ayrı ayrı doğru çalışsa bile birleştirildiklerinde entegrasyon sorunları oluşabilir. Bu nedenle farklı test seviyelerine ihtiyaç duyulur.

### Yanlış 4: %100 test kapsamı, hiç hata olmadığı anlamına gelir.

**Doğrusu:** Test kapsamı, belirlenen kapsam ölçütlerinin ne ölçüde karşılandığını gösterir. %100 kapsam, tüm olası kusurların bulunduğunu veya tüm cihazların ve koşulların test edildiğini garanti etmez.

### Yanlış 5: Bütün olası senaryolar test edilebilir.

**Doğrusu:** Girdi, cihaz, kullanıcı rolü, ortam ve işlem kombinasyonlarının sayısı çok büyük olabilir. Bu nedenle risk analizi ve önceliklendirme yapılır.

### Yanlış 6: Test yalnızca yazılım çalıştırıldığında yapılır.

**Doğrusu:** Test faaliyetleri, yazılım çalıştırılmadan önce gereksinimlerin, tasarımın ve kodun incelenmesini de kapsayabilir.

## 5. Statik Test ve Dinamik Test

### Statik Test

Yazılımı çalıştırmadan iş ürünlerini inceleme faaliyetidir.

Örnekler:

* Gereksinim incelemesi
* Tasarım incelemesi
* Kod incelemesi
* Dokümantasyon incelemesi

### Dinamik Test

Yazılımı çalıştırarak girdiler, işlemler ve çıktılar üzerinden davranışını değerlendirmektir.

Örnekler:

* Kullanıcı girişi test etmek
* Sepete ürün eklemek
* API isteği gönderip yanıtı kontrol etmek
* Hatalı veri girildiğinde sistemin davranışını incelemek

## 6. Test Uzmanının Bakış Açısı

Bir hata üretim ortamında ortaya çıktığında hemen test uzmanını suçlamak doğru değildir. Öncelikle kök neden araştırılmalıdır.

Olası nedenler:

* Gereksinimlerin eksik veya belirsiz olması
* Test kapsamının yetersiz kalması
* Zaman veya ortam kısıtları
* Bileşenler arasındaki entegrasyon sorunları
* Test sırasında bir kusurun gözden kaçırılması

Test uzmanı kusurları azaltmak için çalışır; bütün kusurların bulunacağını garanti etmez.

## Temel Kavramlar

* **Requirement:** Gereksinim
* **Defect / Bug:** Kusur / hata
* **Test Coverage:** Test kapsamı
* **Static Testing:** Statik test
* **Dynamic Testing:** Dinamik test
* **Unit Testing:** Birim testi
* **Integration Testing:** Entegrasyon testi
* **Beta Testing:** Beta testi
* **Root Cause Analysis:** Kök neden analizi

## Kısa Özet

Yazılım testi yalnızca hata bulmak değil, kalite ve riskler hakkında bilgi edinmek için yürütülen sistematik bir süreçtir. Testler hatasızlığı garanti etmez. Etkili test için farklı test seviyeleri, risk temelli önceliklendirme ve ekip iş birliği gerekir.
