# Gereksinim, Tasarım ve Test Oracle

## 1. Yazılım testinde sadece uygulamayı test etmeyiz

Bir yazılım test uzmanının görevi yalnızca uygulamayı çalıştırıp hata bulmak değildir.

Test sürecinde farklı çalışma ürünlerini incelemek gerekir:

* Gereksinimler
* Kullanıcı hikâyeleri
* Tasarımlar
* Wireframe'ler
* Figma ekranları
* Test senaryoları
* Uygulamanın kendisi

Amaç, bu kaynaklar arasında tutarlılık olup olmadığını kontrol etmek ve uygulamanın beklenen davranışı sağlayıp sağlamadığını değerlendirmektir.

---

## 2. Gereksinimlerden tasarıma

Genellikle süreç şu şekilde ilerler:

**Gereksinim → Tasarım/Wireframe → Geliştirme → Test**

Örneğin bir e-ticaret uygulamasında gereksinim şöyle olabilir:

> Kullanıcı sepetinde en az 1 ürün bulundurabilmelidir.

Bu gereksinime göre oluşturulan tasarımda sepet sayısının `0` olarak gösterilmesi bir tutarsızlık olabilir.

Test uzmanı burada sadece ekrana bakmaz.

Şu soruları sorar:

* Gereksinim ne söylüyor?
* Tasarım gereksinimle uyumlu mu?
* Uygulama tasarıma uygun mu?
* Uygulama gereksinime uygun mu?

---

## 3. Wireframe incelemesinde nelere bakılır?

Wireframe incelerken öncelikle görsel ayrıntılardan çok **öğelerin ve akışın gereksinimlerle uyumuna** bakılır.

Örneğin:

* Gerekli buton var mı?
* Gereksiz bir buton var mı?
* Ürün sayısı doğru şekilde temsil ediliyor mu?
* Kupon alanı gereksinime uygun mu?
* Vergi öncesi ve sonrası toplam gösteriliyor mu?
* Silme işlemi için gerekli onay mekanizması var mı?
* Ödeme yöntemleri gereksinimlerle uyumlu mu?
* Hata mesajları yeterince açık mı?

### Örnek

Gereksinim:

> Kullanıcı yalnızca bir kupon kodu uygulayabilir.

Tasarımda iki kupon kodu girebilme alanı bulunuyorsa:

**Gereksinim ↔ Tasarım arasında tutarsızlık vardır.**

Bu durum geliştirme başlamadan önce fark edilirse, ileride oluşabilecek bir problemi erken aşamada önlemiş oluruz.

---

## 4. Tasarım incelemesinde örnek hatalar

Bir ödeme ekranında:

**Gereksinim:**

* Visa
* Mastercard
* PayPal

destekleniyor.

Ancak tasarımda:

* Visa
* Mastercard
* PayPal
* American Express

gösteriliyorsa American Express'in neden eklendiği sorgulanmalıdır.

Bu doğrudan bir defect olarak raporlanmadan önce ilgili kişiyle doğrulanabilir.

---

## 5. Hata mesajları da test edilir

Bir ödeme başarısız olduğunda:

> "Ödeme hatası. Lütfen tekrar deneyin."

mesajı kullanıcıya yeterli bilgi vermeyebilir.

Daha anlamlı bir hata mesajı:

> "Kartınız reddedildi. Lütfen farklı bir ödeme yöntemi deneyin."

olabilir.

Burada test uzmanı yalnızca mesajın ekranda bulunup bulunmadığına değil, **mesajın kullanıcı için yeterince açıklayıcı olup olmadığına** da bakar.

---

## 6. Gereksinim ile uygulama çelişirse

Temel kural:

> Uygulamanın davranışı açık ve geçerli bir gereksinimle çelişiyorsa, bu durum defect olarak değerlendirilmelidir.

Örneğin gereksinim:

> Sipariş tamamlandığında kullanıcıya onay e-postası gönderilmelidir.

Uygulama:

> Sipariş tamamlanıyor ancak e-posta gönderilmiyor.

Bu durumda defect oluşturulmalıdır.

---

## 7. Ancak gereksinimin güncel olup olmadığı önemlidir

Bazı projelerde gereksinimler güncel olmayabilir.

Örneğin:

> Gereksinim dokümanı uzun zamandır güncellenmemiş olabilir.

Bu durumda test uzmanı körü körüne dokümana bağlı kalmamalıdır.

İlgili kişilerle iletişim kurulmalı ve mevcut davranışın gerçekten beklenen davranış olup olmadığı doğrulanmalıdır.

---

## 8. Gereksinimdeki bir özellik henüz geliştirilmediyse

Burada sprint kapsamı önemlidir.

Örneğin:

**Sprint 1:**

* Login
* Ürün listeleme
* Sepete ürün ekleme

**Sprint 2:**

* Kupon uygulama
* Ödeme

Sprint 1 sırasında kupon özelliğinin bulunmaması defect değildir.

Çünkü özellik henüz geliştirme kapsamında değildir.

Ancak Sprint 2'de kupon özelliğinin bulunması bekleniyor ve geliştirilmemişse, bu durum defect veya tamamlanmamış iş olarak değerlendirilebilir.

### Temel ayrım

**Mevcut sprint kapsamında olması gereken özellik yoksa → sorun**

**Gelecek sprintte geliştirilecek özellik henüz yoksa → defect değildir**

---

## 9. Gereksinimde olmayan bir özellik varsa

Uygulamada gereksinimlerde belirtilmeyen bir özellik bulunabilir.

Örneğin:

Gereksinimlerde ödeme sırasında kredi kartı ve PayPal belirtilmiş olsun.

Uygulamada ayrıca yeni bir ödeme yöntemi eklenmiş olsun.

Hemen defect oluşturmadan önce şu sorular sorulmalıdır:

* Bu özellik planlandı mı?
* Ürün sahibi bu özelliği istedi mi?
* Başka bir toplantıda bu karar alındı mı?
* Gereksinim dokümanı güncellenmedi mi?

Bu nedenle geliştirici, Product Owner veya Business Analyst ile iletişim kurulmalıdır.

---

# 10. Gereksinimlerde bulunmayan önemli bir işlev

Bazen test sırasında gereksinimlerde hiç belirtilmemiş ancak ürün açısından önemli bir işlev fark edilebilir.

Örneğin bir online eğitim platformunda video oynatılıyor.

Ancak:

* Video kalite seçeneği yok.
* Kullanıcı kaliteyi değiştiremiyor.
* İnternet hızına göre kalite değişimi belirtilmemiş.

Bu durum doğrudan "bug" olarak raporlanmak zorunda değildir.

Bunun yerine paydaşlara şu soru yöneltilebilir:

> "Video kalite seçeneğinin kullanıcıya sunulması gerekiyor mu?"

Bu özellik Product Backlog'a alınabilir ve ilerleyen sprintlerde geliştirilebilir.

Buradaki önemli nokta:

> Test uzmanı yalnızca mevcut gereksinimleri doğrulamaz; eksik veya riskli gereksinimleri de görünür hale getirebilir.

---

# 11. Defect mi, öneri mi?

Her problem defect değildir.

Örneğin ödeme süreci teknik olarak çalışıyor olabilir ancak kullanıcı açısından gereğinden fazla uzun olabilir.

Test uzmanı bunu:

**Defect**

yerine

**Improvement / Suggestion**

olarak raporlayabilir.

Örneğin:

* Ödeme adımlarının azaltılması
* Buton yerleşiminin iyileştirilmesi
* Renk kontrastının artırılması
* Gereksiz alanların kaldırılması
* Kullanıcı akışının sadeleştirilmesi

gibi öneriler sunulabilir.

Bu yaklaşım test uzmanının yalnızca "bug bulan kişi" olmadığını gösterir.

---

# 12. Gereksinim ve tasarım çelişirse ne yapmalıyız?

Bu durumda hemen:

> "Gereksinim doğrudur, tasarım yanlıştır."

demek doğru değildir.

Çünkü projeye göre tasarım önce hazırlanmış olabilir.

Örneğin:

**Tasarım → Gereksinimlerin yazılması → Geliştirme**

şeklinde bir süreç de olabilir.

Bu nedenle önce projenin **doğruluk kaynağını** belirlemek gerekir.

Burada önemli kavram:

# Test Oracle

## 13. Test Oracle nedir?

**Test Oracle**, test uzmanının bir işlevin beklenen sonucunu belirlemek için başvurduğu bilgi kaynağıdır.

Basitçe:

> "Bu uygulama nasıl davranmalı?"

sorusunun cevabını nereden aldığımızdır.

Test Oracle aşağıdakilerden biri olabilir:

* Functional Requirements
* User Stories
* Acceptance Criteria
* Product Backlog
* Figma Design
* Wireframe
* Teknik dokümantasyon
* Müşteri
* Product Owner
* Business Analyst
* Diğer yetkili paydaşlar

---

## 14. Test Oracle neden önemlidir?

Bir test uzmanı şu iki kaynak arasında çelişki gördüğünde:

**Requirement:**

> Kullanıcı tek kupon kullanabilir.

**Design:**

> Kullanıcı iki kupon girebilir.

Test uzmanı kendi fikrine göre karar vermemelidir.

Önce:

> "Bu durumda hangi kaynak doğru kabul ediliyor?"

sorusunun cevabı bulunmalıdır.

Product Owner, Business Analyst veya müşteri doğru kaynağı belirleyebilir.

---

# 15. Test uzmanının eleştirel bakış açısı

İyi bir test uzmanı yalnızca:

> "Gereksinimde ne yazıyor?"

diye bakmaz.

Aynı zamanda:

* Bu gereksinim yeterli mi?
* Tasarım gereksinimle uyumlu mu?
* Kullanıcı açısından mantıklı mı?
* Eksik bir senaryo var mı?
* Çelişen bilgiler var mı?
* Bu davranış gerçekten isteniyor mu?
* Kullanıcı açısından risk oluşturuyor mu?
* Gereksinim güncel mi?

gibi sorular sorar.

Bu nedenle yazılım testinde **critical thinking / eleştirel düşünme** önemli bir beceridir.

---

# 16. Test uzmanının temel yaklaşımı

Test sürecinde şu zincir kullanılabilir:

**Requirement**
↓
**Design / Wireframe**
↓
**Test Scenario**
↓
**Test Case**
↓
**Execution**
↓
**Expected Result vs Actual Result**
↓
**Defect / Improvement / Clarification**

Ve her aşamada temel soru:

> **"Beklenen davranışın kaynağı nedir?"**

Bu sorunun cevabı test uzmanının doğru karar vermesini sağlar.

---

