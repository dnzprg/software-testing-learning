# Yazılım Test Türleri

## 1. İşlevsel Test (Functional Testing)

Yazılımın ne yaptığını ve işlevlerinin belirtilen gereksinimleri karşılayıp karşılamadığını kontrol eder.

**Örnekler:**

* Geçerli kullanıcı bilgileriyle giriş yapılabilmesi
* Geçersiz parolanın reddedilmesi
* Ürünün sepete eklenmesi
* Ödeme işleminin tamamlanması

Test temeli olarak gereksinimler, kullanıcı hikâyeleri, kabul kriterleri ve iş kuralları kullanılabilir.

## 2. İşlevsel Olmayan Test (Non-functional Testing)

Yazılımın nasıl çalıştığını ve kalite özelliklerini değerlendirir.

Başlıca alanlar:

* **Performans testi:** Yanıt süresi ve yük altındaki davranış
* **Güvenlik testi:** Yetkisiz erişim ve güvenlik riskleri
* **Kullanılabilirlik testi:** Sistemin kolay ve anlaşılır kullanılması
* **Erişilebilirlik testi:** Farklı kullanıcıların sistemi kullanabilmesi
* **Güvenilirlik testi:** Sistemin belirli koşullarda kararlı çalışması

Örnek: Bir sayfanın 1.000 eş zamanlı kullanıcı altında belirlenen yanıt süresi hedefini karşılayıp karşılamadığını kontrol etmek.

## 3. Kara Kutu, Beyaz Kutu ve Gri Kutu Testleri

### Kara Kutu Testi (Black-box Testing)

Sistemin iç kodunu bilmeden, girdiler ve gözlemlenebilir çıktılar üzerinden test yapılır.

Örnek: Giriş ekranına geçerli ve geçersiz bilgiler girerek sonuçları kontrol etmek.

### Beyaz Kutu Testi (White-box Testing)

Sistemin iç yapısı, kodu veya kontrol akışı hakkında bilgi kullanılarak test yapılır.

Örnek: Bir geliştiricinin koşullu ifadelerin farklı dallarını çalıştıracak birim testleri hazırlaması.

### Gri Kutu Testi (Grey-box Testing)

Test uzmanının sistemin iç yapısı hakkında kısmi bilgiye sahip olduğu yaklaşımdır.

Örnek: Kaynak koduna erişmeden API sözleşmelerini, veri yapısını veya sistem mimarisini dikkate alarak test yapmak.

**Önemli:** Kara kutu ve beyaz kutu, test yaklaşımını; statik ve dinamik test ise test faaliyetinin nasıl gerçekleştirildiğini anlatır. Bunlar aynı sınıflandırma değildir.

## 4. Statik ve Dinamik Test

### Statik Test (Static Testing)

Yazılım çalıştırılmadan iş ürünlerinin incelenmesidir.

Örnekler:

* Gereksinim incelemesi
* Tasarım incelemesi
* Kod incelemesi
* Test senaryolarının gözden geçirilmesi
* Yapay zekânın oluşturduğu test senaryolarının doğrulanması

### Dinamik Test (Dynamic Testing)

Yazılım çalıştırılarak davranışının değerlendirilmesidir.

Örnekler:

* Giriş işlemini gerçekleştirmek
* API isteği gönderip yanıtı kontrol etmek
* Sepet ve ödeme akışını test etmek

Dinamik test kara kutu veya beyaz kutu yaklaşımıyla gerçekleştirilebilir.

## 5. Yeniden Test (Retesting / Confirmation Testing)

Daha önce bir kusur nedeniyle başarısız olan testin, düzeltme yapıldıktan sonra yeniden yürütülmesidir.

Amaç, bildirilen kusurun gerçekten giderildiğini doğrulamaktır.

**Örnek:** Geçerli parola ile giriş yapılamadığı için hata raporu oluşturuldu. Geliştirici düzeltme yaptıktan sonra aynı test senaryosu yeniden çalıştırılır.

## 6. Regresyon Testi (Regression Testing)

Bir değişiklikten sonra mevcut işlevlerin olumsuz etkilenmediğini kontrol eder.

**Örnek:** Ödeme modülünde değişiklik yapıldıktan sonra ödeme işleminin yanı sıra sepet tutarı, indirimler ve sipariş oluşturma gibi ilişkili işlevler de kontrol edilir.

Regresyon testleri manuel veya otomatik yürütülebilir. Sık tekrarlanan regresyon senaryoları otomasyon için uygun adaylar olabilir.

### Retest ve Regresyon Arasındaki Fark

* **Retest:** Belirli kusurun düzeltildiğini doğrular.
* **Regresyon:** Değişikliğin başka işlevleri bozmadığını kontrol eder.

## 7. Duman Testi (Smoke Testing)

Yeni bir yazılım derlemesinin temel işlevlerinin çalışıp çalışmadığını ve daha kapsamlı testlere devam etmek için yeterince kararlı olup olmadığını kontrol eden başlangıç testidir.

Örnekler:

* Uygulama açılıyor mu?
* Kullanıcı giriş yapabiliyor mu?
* Ana sayfa yükleniyor mu?
* Temel sipariş akışı çalışıyor mu?

Amaç, büyük sorunları erken belirleyerek kararsız bir derleme üzerinde kapsamlı test için zaman harcanmasını önlemektir.

## 8. Akıl Sağlığı Testi (Sanity Testing)

Belirli bir değişiklik, düzeltme veya sınırlı işlev alanının beklenen şekilde çalıştığını hızlıca değerlendirmeye odaklanır.

Örnek: Tarih seçici hatası düzeltildikten sonra ilgili tarih seçimi ve bağlantılı temel davranışlar kontrol edilir.

### Duman ve Akıl Sağlığı Testi Arasındaki Fark

* **Smoke:** Yeni derlemenin temel işlevlerini genel olarak kontrol eder.
* **Sanity:** Belirli bir değişiklik veya işlev alanına odaklanır.

Bu terimlerin kullanımı ekipler ve projeler arasında değişebilir; önemli olan testin amacı ve kapsamıdır.

## 9. Özet Tablo

| Test türü      | Temel amaç                                                  |
| -------------- | ----------------------------------------------------------- |
| Functional     | İşlevler gereksinimleri karşılıyor mu?                      |
| Non-functional | Performans, güvenlik ve diğer kalite özellikleri uygun mu?  |
| Black-box      | İç kodu bilmeden davranış doğru mu?                         |
| White-box      | İç yapı ve kontrol akışı uygun şekilde test ediliyor mu?    |
| Grey-box       | Kısmi iç bilgiyle davranış değerlendiriliyor mu?            |
| Static         | İş ürünleri çalıştırılmadan inceleniyor mu?                 |
| Dynamic        | Çalışan yazılımın davranışı doğru mu?                       |
| Retest         | Düzeltilen kusur giderildi mi?                              |
| Regression     | Değişiklik başka işlevleri bozdu mu?                        |
| Smoke          | Yeni derlemenin temel işlevleri çalışıyor mu?               |
| Sanity         | Belirli değişiklik veya alan beklenen şekilde çalışıyor mu? |

## Kısa Özet

Test türleri farklı amaçlara hizmet eder. Doğru test yaklaşımı; gereksinimlere, risklere, değişikliklere ve test edilen sistemin özelliklerine göre seçilir. Test uzmanı yalnızca test yapmakla kalmaz, hangi testin neden gerekli olduğunu da açıklayabilmelidir.
