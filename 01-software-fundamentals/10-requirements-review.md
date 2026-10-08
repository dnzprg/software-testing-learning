# Gereksinimlerin Gözden Geçirilmesi (Requirements Review)

## 1. Gereksinim incelemesi neden önemlidir?

Yazılım geliştirme yaşam döngüsünün başında gereksinimler toplanır, ardından tasarım oluşturulur ve kodlama aşamasına geçilir.

Test uzmanı, kod yazılmadan önce gereksinimlere ve tasarımlara erişmelidir. Bunun iki temel amacı vardır:

1. Gereksinimlerdeki ve tasarımlardaki belirsizlikleri, eksiklikleri ve sorunları tespit etmek.
2. Gereksinimlerden ve tasarımlardan test senaryoları ile test durumları oluşturmak.

Sorunları geliştirme sürecinin başında tespit etmek, bunların tasarıma ve koda taşınmasını önlemeye yardımcı olur.

## 2. Gereksinimlerde karşılaşılan sorunlar

### 2.1 Belirsiz gereksinimler (Ambiguous Requirements)

Bir gereksinimin birden fazla şekilde yorumlanabilmesi durumudur. Geliştirici, aynı ifadeyi farklı biçimlerde uygulayabilir. Bu nedenle gereksinimin açıklığa kavuşturulması gerekir.

**Örnek:** “Sepet, her ürün için doğru fiyatı göstermelidir.”

Burada bazı sorular ortaya çıkar:

* Baz fiyat mı, indirimli fiyat mı gösterilecek?
* Birim fiyat ile ürünün toplam fiyatı ayrı ayrı gösterilecek mi?
* İndirim öncesi ve indirim sonrası fiyatlar nasıl sunulacak?

**İyileştirilmiş gereksinim:**

“Sepette her ürün için baz fiyat, varsa indirimli fiyat ve birim fiyat görüntülenmelidir.”

### 2.2 Eksik gereksinimler (Missing Requirements)

Bir işlevin nasıl çalışacağına ilişkin gerekli ayrıntıların gereksinimlerde yer almamasıdır.

**Örnek:** “Kullanıcılar ürün miktarını güncelleyebilir.”

Bu ifade, izin verilen miktar aralığını belirtmez.

Netleştirilmiş gereksinim örneği:

* Minimum miktar 1, maksimum miktar 99'dur.
* Miktar 0 olarak girildiğinde ürün sepetten kaldırılır.

Eksik gereksinimleri tespit etmek için yalnızca belirtilen davranışlara değil, belirtilmeyen durumlara da dikkat etmek gerekir.

## 3. E-ticaret uygulaması üzerinden gereksinim incelemesi

### 3.1 Alışveriş sepeti

| İlk gereksinim                             | Sorun                                        | Netleştirilmiş gereksinim                                                                              |
| ------------------------------------------ | -------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| Sepet doğru fiyatı göstermelidir.          | “Doğru fiyat” belirsizdir.                   | Baz fiyat, varsa indirimli fiyat ve birim fiyat belirtilir.                                            |
| Kullanıcı ürün miktarını güncelleyebilir.  | Minimum ve maksimum miktar belirtilmemiştir. | Minimum 1, maksimum 99; miktar 0 olursa ürün kaldırılır.                                               |
| Ürün kaldırılırken onay gerekir.           | Onayın nasıl alınacağı belli değildir.       | “Kaldır” ve “İptal” seçenekleri olan bir pencere kullanılır.                                           |
| Sepet toplamına geçerli vergiler dahildir. | Verginin nasıl gösterileceği belirsizdir.    | Ara toplam vergi öncesi gösterilir, vergi ayrı satırda belirtilir ve nihai toplam ikisini birleştirir. |

### 3.2 Ödeme süreci

**İlk gereksinim:** “Ödeme başarısız olursa sistem hatayı ele almalıdır.”

Bu ifade, sistemin nasıl davranacağını açıklamaz.

Netleştirilmesi gerekenler:

* Kullanıcıya hangi hata mesajı gösterilecek?
* Sepet içeriği korunacak mı?
* Kullanıcıdan ücret alınacak mı?
* Kullanıcı tekrar deneyebilecek veya başka bir ödeme yöntemi seçebilecek mi?

**Netleştirilmiş gereksinim örneği:**

“Ödeme başarısız olduğunda sistem, yetersiz bakiye veya kart reddedildi gibi uygun bir hata mesajı göstermelidir. Sepet içeriği korunmalı, başarısız işlem için kullanıcıdan ücret alınmamalı ve yeniden deneme ya da farklı ödeme yöntemi seçme olanağı sunulmalıdır.”

### 3.3 Giriş yapmamış kullanıcılar

**İlk gereksinim:** “Ödeme işlemini tamamlamak için kullanıcıların oturum açmış olması gerekir.”

Bu ifade, giriş yapmamış bir kullanıcının ödeme seçeneğine tıklaması durumunda ne olacağını açıklamaz.

Netleştirilmiş gereksinim:

“Ödeme seçeneğine tıklayan misafir kullanıcı giriş sayfasına yönlendirilir. Giriş yapmadan önce sepete eklediği ürünler korunur.”

### 3.4 Sipariş onay e-postası

**İlk gereksinim:** “Başarılı siparişten sonra onay e-postası gönderilir.”

Belirsiz noktalar:

* E-posta ne zaman gönderilecek?
* Hangi adrese gönderilecek?
* E-postada hangi bilgiler yer alacak?

Netleştirilmiş gereksinim:

“Başarılı siparişten sonra beş dakika içinde kullanıcının kayıtlı e-posta adresine; sipariş özeti, toplam tutar ve tahmini teslimat tarihini içeren bir onay e-postası gönderilir.”

### 3.5 Siparişlerin işleme alınma zamanı

**İlk gereksinim:** “Günlük son saatten sonra verilen siparişler bir sonraki iş günü işleme alınır.”

Burada günlük son saatin kaç olduğu belirtilmemiştir.

Dersin örneğinde gereksinim şu şekilde netleştirilmiştir:

* Hafta içi saat 17.00'den önce verilen siparişler aynı gün işleme alınır.
* Saat 17.00'de veya sonrasında verilen siparişler, hafta sonu verilen siparişler ve resmî tatillerde verilen siparişler bir sonraki iş günü işleme alınır.

Ancak her projede bu kuralın sabit olması gerekmez. Birden fazla müşteriye hizmet veren SaaS uygulamasında günlük son saat müşteriye göre değişebilir. Bu durumda kuralın yapılandırılabilir olması gerekebilir.

**Test uzmanının görevi:** Gereksinimi hemen hatalı ilan etmek yerine, projenin ihtiyaçlarını anlamak ve hangi davranışın beklendiğini netleştirmektir.

## 4. İndirim ve kupon gereksinimlerini incelemek

### 4.1 Kupon kodunun uygulanması

**İlk gereksinim:** “Kullanıcılar ödeme sırasında kupon uygulayabilir.”

Netleştirilmesi gereken sorular:

* Kullanıcı kupon kodunu kendisi mi girecek?
* Kuponlar arasından seçim mi yapacak?
* Aynı siparişte birden fazla kupon kullanılabilecek mi?
* İkinci kupon girildiğinde ilk kuponun yerini mi alacak?

Netleştirilmiş gereksinim örneği:

“Kullanıcılar ödeme öncesinde belirlenen alana kupon kodu girebilir. Sipariş başına yalnızca bir kupon uygulanabilir. İkinci bir kupon girilmeye çalışıldığında onay istenir ve onay verilirse ilk kuponun yerini alır.”

### 4.2 Kuponun kullanım sınırları

“Sipariş başına yalnızca bir kupon uygulanabilir” ifadesi, kuponun kaç farklı kullanıcı tarafından kullanılabileceğini açıklamaz.

Şu ayrım netleştirilmelidir:

* Bir siparişte kullanılabilecek kupon sayısı.
* Aynı kuponun toplam kaç kullanıcı tarafından kullanılabileceği.

Bunlar farklı gereksinimlerdir ve birbirine karıştırılmamalıdır.

### 4.3 Süresi dolmuş kuponlar

**İlk gereksinim:** “Süresi dolmuş kuponlar reddedilmelidir.”

Netleştirilmesi gerekenler:

* Kullanıcıya hangi mesaj gösterilecek?
* Kupon reddedildiğinde sepet toplamı değişecek mi?

Dersin örneğinde, süresi dolmuş kupon reddedilir, kullanıcıya bir mesaj gösterilir ve sepet toplamı değişmeden kalır.

### 4.4 İndirim ve vergi hesaplaması

Dersin örneğinde indirimler, vergiler hesaplanmadan önce sepet ara toplamına uygulanır.

Örneğin:

* Ürün ara toplamı: 9 TL
* Sabit indirim: 10 TL

Bu durumda indirim sonrası tutarın nasıl hesaplanacağı açıkça belirtilmelidir. Dersin revize edilmiş gereksiniminde, indirim ara toplamı sıfıra getirirse verginin ve sipariş toplamının da sıfır olacağı belirtilir.

Bu tür sınır durumları, test uzmanının gereksinim incelemesinde dikkat etmesi gereken önemli noktalardır.

## 5. Gereksinim incelemesi sırasında test uzmanının yaklaşımı

Test uzmanı gereksinimleri değiştirilemez ve sorgulanamaz belgeler olarak görmemelidir. Gereksinimler insanlar tarafından hazırlanır; yeterince incelenmemiş veya eksik bırakılmış olabilir.

Test uzmanı:

1. Belirsiz ifadeleri belirlemelidir.
2. Eksik senaryoları ve iş kurallarını sorgulamalıdır.
3. Gereksinimleri tasarımla karşılaştırmalıdır.
4. Açıklığa kavuşturulması gereken noktaları ilgili kişilerle görüşmelidir.
5. Test senaryolarını oluşturmak için gerekli kararları ve açıklamaları not etmelidir.

Her gereksinim sorunu için doğrudan hata kaydı açılması gerekmez. Bazı konular toplantıda soru olarak gündeme getirilerek netleştirilir.

## 6. Portföy ve mülakat açısından önemli çıkarımlar

Gereksinim incelemesi, test uzmanının yalnızca uygulamayı kullanan kişi olmadığını gösterir. Test uzmanı, yazılım geliştirilmeden önce olası sorunları fark ederek kaliteye katkıda bulunur.

Bir mülakatta şu yaklaşım açıklanabilir:

“Gereksinimleri incelerken belirsiz ifadeleri, eksik iş kurallarını ve belirtilmeyen sınır durumlarını belirlerim. Gerekli noktaları ürün sahibi veya ilgili ekip üyeleriyle netleştirir, alınan kararları test senaryolarıma yansıtırım.”

## 7. Kısa tekrar

* **Belirsiz gereksinim:** Birden fazla şekilde yorumlanabilir.
* **Eksik gereksinim:** Beklenen davranışın gerekli ayrıntıları belirtilmemiştir.
* **Sınır durumu:** Minimum, maksimum, sıfır veya geçersiz değer gibi özel durumlar değerlendirilmelidir.
* **Gereksinim incelemesi:** Sorunları kodlama ve test aşamasından önce fark etmeye yardımcı olur.
* **Test uzmanının rolü:** Soruları belirlemek, açıklama istemek ve netleşen kuralları test senaryolarına dönüştürmektir.

**Temel fikir:** İyi bir test uzmanı yalnızca “Yazılım doğru çalışıyor mu?” diye sormaz. Önce “Doğru çalışması tam olarak ne anlama geliyor?” sorusunu da sorar.
