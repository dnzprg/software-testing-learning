# Çok Rollü ve Çok Kanallı Sistemler

## 1. Yazılım Testi Neden Sadece Uygulamayı Kullanmak Değildir?

Yazılım testi yalnızca uygulamayı bir kullanıcı gibi kullanıp hataları bulmaktan ibaret değildir.

Modern uygulamalar genellikle birden fazla kullanıcı rolü, cihaz, kanal ve sistem bileşeni içerir.

Bu nedenle test uzmanı;

- farklı kullanıcı rollerini,
- farklı cihaz ve kanalları,
- roller arasındaki etkileşimleri,
- pozitif ve negatif senaryoları,
- edge case'leri,
- riskleri

birlikte değerlendirmelidir.

---

## 2. Çok Rollü Sistemler

Bir uygulamada farklı kullanıcıların farklı yetki ve sorumlulukları varsa sistem çok rollü olarak değerlendirilebilir.

Örneğin bir online eğitim platformunda:

### Öğrenci
- Dersleri görüntüler.
- Videoları izler.
- Sınavlara girer.
- Sertifikasını görüntüler.

### Eğitmen
- Kurs oluşturur.
- Ders yükler.
- Öğrencileri görüntüler.
- Öğrenci sonuçlarını inceler.

### Yönetici
- Kullanıcıları yönetir.
- Eğitmenleri yönetir.
- Raporları görüntüler.
- Kullanıcı hesaplarını aktif/pasif hale getirir.

Test sırasında yalnızca her rolün kendi işlemlerinin çalışması değil, **roller arasındaki etkileşimler** de kontrol edilmelidir.

---

## 3. Roller Arasındaki Etkileşim

Örneğin:

1. Yönetici eğitmen hesabı oluşturur.
2. Eğitmen sisteme giriş yapar.
3. Eğitmen kurs oluşturur.
4. Öğrenci kursa kayıt olur.
5. Öğrenci dersleri tamamlar.
6. Öğrenci sınava girer.
7. Eğitmen sonucu görüntüler.
8. Öğrenci başarılı olursa sertifika oluşturulur.

Burada bir kullanıcının yaptığı işlem başka kullanıcıların gördüğü verileri veya sistem durumunu değiştirebilir.

Bu nedenle test uzmanı şu soruyu sormalıdır:

> **"Bu işlem diğer kullanıcıları ve sistemin diğer bölümlerini nasıl etkiliyor?"**

---

## 4. Çok Kanallı Sistemler

Bir sisteme farklı cihaz veya platformlardan erişilebiliyorsa çok kanallı bir yapıdan söz edilebilir.

Örneğin:

- Web
- Android
- iOS
- Tablet
- Akıllı saat

Aynı işlemin farklı kanallarda tutarlı çalışıp çalışmadığı test edilmelidir.

---

## 5. Örnek: Yemek Sipariş Sistemi

Sistemde üç temel rol olduğunu düşünelim:

- Müşteri
- Restoran
- Kurye

Müşteri sipariş verir.

Restoran siparişi kabul eder ve hazırlar.

Kurye siparişi teslim alır ve müşteriye ulaştırır.

### Sipariş iptal edildiğinde

Test yalnızca müşterinin siparişi iptal edip edemediğini kontrol etmekle sınırlı değildir.

Aşağıdaki durumlar da kontrol edilmelidir:

- Restorana bildirim gidiyor mu?
- Kuryeye bildirim gidiyor mu?
- Sipariş durumu tüm kanallarda güncelleniyor mu?
- Web uygulamasında doğru durum gösteriliyor mu?
- Android uygulamasında doğru durum gösteriliyor mu?
- iOS uygulamasında doğru durum gösteriliyor mu?
- Restoran sisteminde sipariş kapanıyor mu?

Bu, **uçtan uca (end-to-end) düşünme** yaklaşımına örnektir.

---

## 6. Edge Case'ler

Test uzmanı yalnızca normal akışı düşünmemelidir.

Örneğin:

- Kullanıcı ödeme sırasında internet bağlantısını kaybederse?
- Sipariş tam iptal edilirken restoran siparişi kabul ederse?
- Aynı işlem iki kez gönderilirse?
- Kullanıcının oturumu işlem sırasında sona ererse?
- Aynı hesap farklı cihazlardan kullanılırsa?

gibi durumlar da değerlendirilmelidir.

Bu tür normal akışın dışında kalan durumlar **edge case** olarak ele alınabilir.

---

## 7. Risk Bazlı Test ve Önceliklendirme

Gerçek projelerde bütün senaryoları aynı anda test etmek mümkün olmayabilir.

Bu nedenle test uzmanı:

> **"Önce neyi test etmeliyim?"**

sorusuna cevap vermelidir.

Öncelik verilebilecek alanlar:

- Kritik işlevler
- Ödeme işlemleri
- Güvenlik açısından önemli işlemler
- Çok kullanılan özellikler
- Birçok sistemi etkileyen işlemler
- Daha önce hata çıkan alanlar

Bu yaklaşım **risk bazlı test (Risk-Based Testing)** düşüncesiyle ilişkilidir.

---

## 8. QA Perspektifi

Bir test uzmanının düşünme şekli yalnızca:

> "Butona bastım, çalışıyor."

olmamalıdır.

Daha kapsamlı yaklaşım:

> **"Bu işlemi hangi kullanıcı yapabilir, hangi koşullarda yapabilir, işlem sonrasında sistemin diğer bölümlerinde ne değişmeli ve diğer kullanıcılar bu değişikliği nasıl görmeli?"**

şeklindedir.

Bu nedenle yazılım testinde teknik bilginin yanında;

- analitik düşünme,
- senaryo oluşturma,
- risk değerlendirme,
- önceliklendirme,
- sistemler arası ilişkiyi anlayabilme

önemlidir.

---

## 🔑 Öğrenilen Temel Kavramlar

| Kavram | Açıklama |
|---|---|
| **Multi-Role** | Birden fazla kullanıcı rolünün bulunması |
| **Multi-Channel** | Birden fazla cihaz veya platform üzerinden erişim |
| **Interaction** | Kullanıcılar ve sistem bileşenleri arasındaki etkileşim |
| **Edge Case** | Normal akışın dışında kalan durum |
| **Prioritization** | Testlerin önem ve risk seviyesine göre sıralanması |
| **End-to-End Testing** | Bir işlemin başlangıçtan sonuca kadar tüm akışının test edilmesi |
| **Risk-Based Testing** | Test önceliğinin risklere göre belirlenmesi |

---

## 🎯 Kısa Özet

> **Yazılım testinin zorluğu yalnızca bir özelliğin çalışıp çalışmadığını kontrol etmek değildir. Farklı rollerin, kanalların ve işlemlerin birbirleriyle olan etkileşimlerini ve olası sonuçlarını sistematik olarak değerlendirmek gerekir.**
