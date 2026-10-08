# Test Süreci ve Test Seviyeleri

## 1. Test Etme ve Hata Ayıklama Arasındaki Fark

**Test etme (Testing):** Yazılımı değerlendirmek, kusurları ortaya çıkarmak ve kalite hakkında bilgi edinmek amacıyla yapılan faaliyetlerdir.

**Hata ayıklama (Debugging):** Bir kusurun nedenini araştırma, kaynağını belirleme ve yazılımdaki problemi düzeltme sürecidir.

Örnek:

* Test uzmanı giriş ekranında hatalı bir sonuç bulur ve hata raporu oluşturur.
* Geliştirici hatanın nedenini araştırır ve kodu düzeltir.
* Düzeltmeden sonra test uzmanı yeniden test yapar (Retest).
* İlgili alanların etkilenmediğini kontrol etmek için regresyon testi de yapılabilir.

Test etme ile hata ayıklama farklı faaliyetlerdir; ancak birlikte çalışırlar.

## 2. Temel Test Faaliyetleri

### Test Planlama

* Testin kapsamını ve amaçlarını belirleme
* Test yaklaşımını ve öncelikleri belirleme
* Zaman, kaynak ve araçları planlama
* Riskleri ve sorumlulukları değerlendirme

### Test Analizi ve Tasarımı

* Gereksinimleri inceleme
* Test edilebilir koşulları belirleme
* Test senaryoları ve test durumları hazırlama
* Test verilerini ve beklenen sonuçları belirleme
* Gerekli test ortamını ve araçları değerlendirme

### Test Uygulaması

* Test ortamını ve verilerini hazırlama
* Testleri öncelik sırasına göre yürütme
* Gerçek sonuçları beklenen sonuçlarla karşılaştırma
* Kusurları raporlama
* Sonuçları kaydetme ve ilgili testleri tekrar yürütme

Test sürecinde ilerleme izleme, kontrol, sonuçları değerlendirme ve tamamlanma faaliyetleri de bulunur.

## 3. ISTQB'ye Göre Yedi Test Faaliyeti

ISTQB'nin temel test süreci modeli şu faaliyetleri içerir:

1. **Test Planning:** Test planlama
2. **Test Monitoring and Control:** Test izleme ve kontrol
3. **Test Analysis:** Test analizi
4. **Test Design:** Test tasarımı
5. **Test Implementation:** Test uygulamasının hazırlanması
6. **Test Execution:** Test yürütme
7. **Test Completion:** Test tamamlama

Bu faaliyetler her projede mutlaka katı ve doğrusal bir sırayla yürütülmez. Projenin yöntemine ve ihtiyaçlarına göre tekrarlanabilir, örtüşebilir ve uyarlanabilir.

## 4. Test Seviyeleri

Test seviyeleri, yazılımın hangi kapsamda değerlendirildiğini ifade eder.

### 4.1 Birim Testi (Unit Testing)

En küçük test edilebilir yazılım birimlerini değerlendirir.

Örnek: Bir vergi hesaplama fonksiyonunun doğru sonucu üretip üretmediğini kontrol etmek.

Genellikle geliştiriciler tarafından gerçekleştirilir.

### 4.2 Entegrasyon Testi (Integration Testing)

Bileşenler, modüller veya sistemler arasındaki arayüzleri ve etkileşimleri değerlendirir.

Örnek: Giriş modülünün kullanıcı veritabanıyla doğru iletişim kurup kurmadığını kontrol etmek.

Geliştiriciler veya test uzmanları tarafından, testin kapsamına göre gerçekleştirilebilir.

### 4.3 Sistem Testi (System Testing)

Bir sistemi bütün olarak, belirtilen gereksinimlere göre değerlendirir.

Örnek: Bir e-ticaret uygulamasında kullanıcı kaydı, giriş, ürün arama, sepete ekleme ve sipariş oluşturma akışlarını test etmek.

Sistem testi işlevsel ve işlevsel olmayan gereksinimleri kapsayabilir.

### 4.4 Sistem Entegrasyon Testi (System Integration Testing)

Birbirinden ayrı sistemlerin ve harici hizmetlerin birlikte doğru çalışıp çalışmadığını değerlendirir.

Örnek: E-ticaret uygulamasının ödeme sağlayıcısı, kargo sistemi ve e-posta hizmetiyle doğru iletişim kurduğunu kontrol etmek.

### 4.5 Kabul Testi (Acceptance Testing)

Sistemin iş ihtiyaçlarını, kullanıcı gereksinimlerini veya kabul kriterlerini karşılayıp karşılamadığını değerlendirir.

Örnek: İş biriminin sipariş ve iade süreçlerinin belirlenen iş kurallarına uygunluğunu doğrulaması.

**UAT (User Acceptance Testing):** Kullanıcı kabul testi; kabul testinin yaygın bir türüdür. Kabul testi yalnızca UAT ile sınırlı değildir.

## 5. Test Seviyelerine E-Ticaret Örneği

* **Birim testi:** İndirim hesaplama fonksiyonu doğru sonucu üretiyor mu?
* **Entegrasyon testi:** Sepet modülü fiyat hizmetinden doğru tutarı alıyor mu?
* **Sistem testi:** Kullanıcı ürünü seçip siparişi tamamlayabiliyor mu?
* **Sistem entegrasyon testi:** Sipariş ödeme ve kargo sistemlerine doğru iletiliyor mu?
* **Kabul testi:** Sipariş ve ödeme süreci işletmenin belirlediği kuralları karşılıyor mu?

## 6. Önemli Ayrımlar

* Test etme kusurları ortaya çıkarmaya, hata ayıklama ise kusurun nedenini bulup düzeltmeye odaklanır.
* Test seviyeleri yalnızca kimin test yaptığına göre değil, test edilen kapsam ve amaca göre ayrılır.
* Birim testi, entegrasyon testi, sistem testi ve kabul testi farklı amaçlara hizmet eder.
* Uçtan uca (E2E) test, birden fazla bileşen veya sistem boyunca iş akışını doğrulayabilir. Her uçtan uca test otomatik olarak yalnızca sistem testiyle eş anlamlı değildir.
* Testler farklı seviyelerde ve farklı geliştirme yöntemlerinde tekrarlanabilir.

## Temel Kavramlar

* Testing: Test etme
* Debugging: Hata ayıklama
* Test Case: Test durumu
* Test Scenario: Test senaryosu
* Test Plan: Test planı
* Retest: Yeniden test
* Regression Testing: Regresyon testi
* Unit Testing: Birim testi
* Integration Testing: Entegrasyon testi
* System Testing: Sistem testi
* System Integration Testing: Sistem entegrasyon testi
* Acceptance Testing: Kabul testi
* UAT: Kullanıcı kabul testi
* E2E Testing: Uçtan uca test
