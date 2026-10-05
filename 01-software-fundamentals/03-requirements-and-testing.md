# Yazılım Projesi Nasıl Başlar?

## 1. Her şey gereksinimlerle başlar

Bir yazılım projesinin başlangıç noktası **müşterinin ihtiyacıdır**.

Müşteri bir uygulama geliştirmek ister ve neye ihtiyaç duyduğunu anlatır.

Örneğin bir e-ticaret uygulaması yapmak istediğini düşünelim.

Müşterinin ihtiyaçları şöyle olabilir:

* Kullanıcı kayıt olabilmeli.
* Kullanıcı giriş yapabilmeli.
* Profilini yönetebilmeli.
* Ürünleri görüntüleyebilmeli.
* Ürün arayabilmeli.
* Filtreleme yapabilmeli.
* Ürünü sepete ekleyebilmeli.
* Ödeme yapabilmeli.

Bu ihtiyaçların anlaşılması ve belgelenmesi gerekir.

---

# 2. Gereksinimleri kim toplar?

Müşterinin anlattığı ihtiyaçları anlamak ve dokümante etmek genellikle:

* **Business Analyst (İş Analisti)**
* **Product Owner (Ürün Sahibi)**
* veya **Requirements Engineer (Gereksinim Mühendisi)**

gibi rollerin sorumluluğundadır.

Bu kişi müşteriye sorular sorar ve ihtiyaçları netleştirmeye çalışır.

Çünkü müşterinin söylediği her şey başlangıçta net veya doğru olmayabilir.

Örneğin müşteri:

> "Kullanıcı hızlı bir şekilde kayıt olabilsin."

diyebilir.

Burada iş analisti şu soruları sorabilir:

* Hangi bilgiler alınacak?
* Telefon numarası zorunlu mu?
* E-posta zorunlu mu?
* SMS doğrulaması olacak mı?
* Şifre için kurallar var mı?
* Kullanıcı yanlış bilgi girerse ne olacak?

Böylece belirsizlikler azaltılır.

---

# 3. Gereksinimler neden bu kadar önemli?

Çünkü gereksinimler projenin temelini oluşturur.

**Gereksinim → Tasarım → Geliştirme → Test**

sürecinin temelinde gereksinimler vardır.

Geliştirici neyi geliştireceğini gereksinimlerden anlar.

Test uzmanı ise **neyi test edeceğini ve beklenen sonucun ne olduğunu** gereksinimlerden anlar.

Bu nedenle gereksinimlerde bir hata veya belirsizlik varsa bu hata projenin sonraki aşamalarını da etkileyebilir.

---

# 4. Test uzmanı gereksinimleri neden okur?

Test uzmanı sadece geliştirilen uygulamaya bakıp rastgele test yapmaz.

Öncelikle:

> **"Bu uygulama nasıl çalışmalı?"**

sorusunun cevabını öğrenmesi gerekir.

Bunun için gereksinimleri inceler.

Gereksinimlerde belirtilen **beklenen sonuçlar**, test senaryolarının oluşturulmasına temel oluşturur.

---

# 5. Basit bir kullanıcı kaydı örneği

Bir gereksinim şöyle olsun:

> Kullanıcı kayıt olurken telefon numarasını girmeli ve SMS ile gönderilen OTP kodunu doğrulamalıdır.

Beklenen davranış:

1. Kullanıcı telefon numarasını girer.
2. Sistem OTP gönderir.
3. Kullanıcı OTP'yi girer.
4. OTP doğruysa kayıt tamamlanır.
5. OTP yanlışsa hata mesajı gösterilir.
6. OTP girilmeden kayıt tamamlanamaz.

Test uzmanı bu gereksinime göre farklı senaryolar oluşturabilir.

### Pozitif senaryo

Doğru telefon numarası + doğru OTP

**Beklenen sonuç:** Kayıt başarıyla tamamlanır.

### Negatif senaryo

Doğru telefon numarası + yanlış OTP

**Beklenen sonuç:** Hata mesajı gösterilir.

### Başka bir senaryo

OTP hiç girilmez.

**Beklenen sonuç:** Kullanıcı kayıt işlemine devam edemez.

---

# 6. Beklenen Sonuç ve Gerçek Sonuç

Testin temel mantıklarından biri:

**Expected Result (Beklenen Sonuç)**
ile
**Actual Result (Gerçek Sonuç)**

karşılaştırmaktır.

Örneğin:

**Beklenen:** Yanlış OTP girildiğinde hata mesajı gösterilmeli.

**Gerçek:** Yanlış OTP girildiğinde kullanıcı kayıt olabiliyor.

Burada:

**Beklenen sonuç ≠ Gerçek sonuç**

olduğu için test başarısızdır.

---

# 7. Bug nasıl ortaya çıkar?

Gerçek sonuç beklenen sonuçla aynı değilse bir **bug/defect** oluşabilir.

Örneğin:

> Yanlış OTP ile kullanıcı kayıt olabiliyor.

Test uzmanı bu durumu geliştiriciye iletmek için **bug report** oluşturur.

Bug raporunda genellikle:

* Bug başlığı
* Test adımları
* Beklenen sonuç
* Gerçek sonuç
* Öncelik
* Severity
* Ortam bilgisi
* Ekran görüntüsü veya kanıt

gibi bilgiler bulunabilir.

---

# 8. Geliştirici düzeltir, test uzmanı tekrar test eder

Bug geliştiriciye iletildikten sonra geliştirici problemi düzeltir.

Daha sonra test uzmanı tekrar test yapar.

Bu sürece **retest** denir.

Örneğin:

**İlk test:**

Yanlış OTP → Kullanıcı kayıt olabiliyor ❌

**Developer fix**

↓

**Retest:**

Yanlış OTP → Hata mesajı gösteriliyor ✅

Böylece yapılan düzeltmenin gerçekten çalışıp çalışmadığı kontrol edilir.

Ancak test uzmanı burada yalnızca düzeltmeyi tekrar kontrol etmekle kalmaz; yapılan değişikliğin başka işlevleri bozup bozmadığını da değerlendirebilir.

---

# 9. Test uzmanı ile Business Analyst / Product Owner ilişkisi

Test sırasında gereksinimle ilgili belirsizlik ortaya çıkabilir.

Örneğin test uzmanı şöyle bir soru sorabilir:

> "Kullanıcı OTP'yi 5 kez yanlış girerse hesap kilitlenmeli mi?"

Bu bilgi gereksinimde belirtilmemiş olabilir.

Test uzmanı geliştiriciyle konuşabilir ancak iş kuralının ne olması gerektiğini çoğunlukla **Business Analyst veya Product Owner** netleştirir.

Gerekirse konu müşteriye sorulur.

Bu nedenle test uzmanı sadece geliştiriciyle değil, projenin farklı rolleriyle iletişim halindedir.

---

# 10. Test uzmanının temel çalışma döngüsü

Basitleştirirsek süreç şöyle ilerler:

**Müşteri ihtiyacı**

↓

**Gereksinimler**

↓

**Geliştirme**

↓

**Test senaryolarının hazırlanması**

↓

**Test execution**

↓

**Beklenen sonuç / Gerçek sonuç karşılaştırması**

↓

**Bug bulundu mu?**

↓

**Evet → Bug Report**

↓

**Developer Fix**

↓

**Retest**

↓

**Başarılı mı?**

↓

**Evet → Test Passed**

---

# 11. QA Perspektifinden Benim Çıkardığım Sonuç

Bir test uzmanı için gereksinimleri anlamak çok önemlidir.

Çünkü test uzmanının görevi sadece:

> "Uygulama çalışıyor mu?"

diye bakmak değildir.

Asıl soru:

> **"Uygulama, tanımlanan gereksinimlere uygun çalışıyor mu?"**

olmalıdır.

Bu nedenle test uzmanı:

* Gereksinimleri okumalı.
* Belirsizlikleri fark etmeli.
* Sorular sormalı.
* Test senaryoları oluşturmalı.
* Beklenen sonuçları belirlemeli.
* Gerçek sonuçları gözlemlemeli.
* Hataları raporlamalı.
* Düzeltmeleri tekrar test etmeli.
* Gerekirse regresyon testleri yapmalıdır.

---

## 🔑 Akılda Tutmam Gereken 7 Kavram

**1. Requirement:** Gereksinim
**2. Expected Result:** Beklenen sonuç
**3. Actual Result:** Gerçek sonuç
**4. Test Scenario:** Test senaryosu
**5. Bug/Defect:** Beklenen ve gerçek davranış arasındaki problem
**6. Bug Report:** Hatanın kayıt altına alınması
**7. Retest:** Düzeltilen hatanın tekrar test edilmesi

### 🎯 Tek cümlelik özet

> **Yazılım testi, uygulamayı rastgele kullanmak değil; gereksinimlerde tanımlanan beklenen davranışları gerçek sonuçlarla karşılaştırarak yazılımın gereksinimlere uygunluğunu doğrulama sürecidir.**
