# SDLC – Yazılım Geliştirme Yaşam Döngüsü

## 1. SDLC Nedir?

**SDLC (Software Development Life Cycle)**, bir yazılımın fikir aşamasından geliştirilmesine, test edilmesine, yayınlanmasına ve bakımına kadar geçen süreci ifade eder.

Bir yazılım test uzmanı için SDLC'yi bilmek önemlidir çünkü:

* Test sürecinin ne zaman başlayacağını,
* Hangi aşamada hangi test faaliyetlerinin yapılacağını,
* Test ekibinin diğer ekiplerle ne zaman iletişim kuracağını,
* Test çalışmalarının nasıl planlanacağını

anlamamızı sağlar.

---

# 2. Sıralı (Sequential) Geliştirme

Sıralı geliştirmede süreç adım adım ilerler.

Genel olarak:

**Gereksinimler → Tasarım → Kodlama → Test → Yayınlama → Bakım**

şeklindedir.

Bir aşama tamamlandıktan sonra diğer aşamaya geçilir.

Örneğin:

1. Gereksinimler toplanır.
2. Uygulamanın tasarımı yapılır.
3. Kodlama yapılır.
4. Test gerçekleştirilir.
5. Yazılım müşteriye/kullanıcıya sunulur.
6. Yayın sonrası bakım yapılır.

Sıralı geliştirmenin en bilinen modellerinden biri **Waterfall (Şelale)** modelidir.

---

# 3. Waterfall (Şelale) Modeli

Waterfall, sıralı geliştirme modellerinden biridir.

Temel akış:

**Requirements → Design → Development → Testing → Deployment → Maintenance**

Yani:

**Gereksinim → Tasarım → Geliştirme → Test → Yayınlama → Bakım**

### Waterfall'ın temel özelliği

Test, geliştirme aşamasından sonra gelir.

Bu yaklaşımın önemli bir dezavantajı vardır:

> Hatalar geç fark edilebilir.

Örneğin bir gereksinimde hata varsa bu hata:

**Gereksinim → Tasarım → Kodlama**

aşamalarından geçtikten sonra test sırasında ortaya çıkabilir.

Bu durumda hatayı düzeltmek daha fazla zaman ve maliyet gerektirebilir.

---

# 4. Early Testing – Erken Test

Yazılım testinin önemli prensiplerinden biri:

> **Testing should start early.**

Yani:

> **Test faaliyetleri mümkün olduğunca erken başlamalıdır.**

Test etmek için kodun tamamlanmasını beklemek zorunda değiliz.

Örneğin gereksinimler daha yazılırken onları inceleyebiliriz.

Şu soruları sorabiliriz:

* Gereksinimler açık mı?
* Birbirleriyle çelişiyor mu?
* Eksik bilgi var mı?
* Belirsiz ifadeler var mı?
* Test edilebilir mi?
* Gereksinim gerçekten uygulanabilir mi?

Aynı şekilde tasarım da geliştirme başlamadan önce incelenebilir.

Dolayısıyla test uzmanının katkısı **kod yazıldıktan sonra başlamaz.**

Test uzmanı daha erken aşamalarda projeye dahil olabilir.

---

# 5. V-Model

Waterfall'ın bu problemlerinden dolayı **V-Model** yaklaşımı önem kazanır.

V-Model de sıralı bir geliştirme modelidir ancak önemli bir farkı vardır:

> **Her geliştirme aşamasının karşısında ilişkili bir test seviyesi bulunur.**

Basitleştirilmiş hali:

| Geliştirme Aşaması          | İlgili Test           |
| --------------------------- | --------------------- |
| Kullanıcı gereksinimleri    | Acceptance Testing    |
| Sistem/Teknik gereksinimler | System Testing        |
| Yüksek seviye tasarım       | Integration Testing   |
| Detaylı/modül tasarımı      | Unit Testing          |
| Kodlama                     | Testlerin uygulanması |

Buradaki temel fikir:

**Testi sonradan düşünmek yerine, test faaliyetlerini daha projenin başından planlamak.**

---

# 6. V-Model'de Test Uzmanının Rolü

Önemli bir nokta:

Testlerin **planlanması ve tasarlanması** erken başlayabilir.

Ancak testlerin gerçekten **çalıştırılması (test execution)** için genellikle test edilebilir bir yazılım veya ilgili bileşenin hazır olması gerekir.

Örneğin gereksinimler yazılırken test uzmanı:

* Test senaryolarını planlayabilir.
* Gereksinimleri analiz edebilir.
* Beklenen sonuçları belirleyebilir.
* Belirsizlikleri sorgulayabilir.
* Test koşullarını oluşturabilir.

Kod henüz hazır olmadığı için uygulamayı çalıştırarak test etmek ise daha sonra mümkün olur.

---

# 7. Agile (Çevik) Geliştirme

Sıralı modellerde bütün uygulama için uzun bir geliştirme süreci olabilir.

Agile yaklaşımında ise büyük proje daha küçük parçalara bölünür.

Bu parçalara:

* **Sprint**
* **Iteration (Yineleme)**
* **Increment (Artım)**

gibi isimler verilebilir.

Örneğin bir yıl sürecek bir projeyi tek seferde tamamlamak yerine daha küçük dönemlere ayırabiliriz.

Her dönem içerisinde:

**Gereksinim → Tasarım → Geliştirme → Test → Yayınlama**

gibi bir döngü tekrar edilir.

Bu sayede çalışan yazılım daha erken elde edilebilir ve müşteriden geri bildirim alınabilir.

---

# 8. Iterative Development – Yinelemeli Geliştirme

Iterative geliştirmede amaç, mevcut ürünü tekrar tekrar geliştirerek daha iyi hale getirmektir.

Örneğin:

### Iteration 1

Temel çalışan ürün oluşturulur.

### Iteration 2

Mevcut ürüne yeni özellikler eklenir.

### Iteration 3

Daha fazla özellik ve iyileştirme yapılır.

### Iteration 4

Ürün daha da geliştirilir.

Yani:

**Çalışan ürün → Daha iyi ürün → Daha gelişmiş ürün → Daha iyi ürün**

şeklinde ilerler.

### Ana fikir:

> **İlk yinelemenin sonunda kullanılabilir bir ürün elde edilebilir ve sonraki yinelemelerde bu ürün geliştirilir.**

---

# 9. Incremental Development – Artımlı Geliştirme

Incremental geliştirmede ise ürün **parçalar halinde oluşturulur.**

Örneğin bir araba yapacağımızı düşünelim.

İlk aşamada:

* Tekerlek

sonra:

* Şasi

sonra:

* Motor

sonra:

* Diğer parçalar

eklenerek sonunda bütün araba oluşturulur.

Buradaki önemli nokta:

> İlk parçalar tek başına tamamlanmış ve kullanılabilir bir ürün olmayabilir.

Yani müşteriye ilk artımı verdiğimizde gerçek ürünü kullanamayabilir.

---

# 10. Iterative ve Incremental Farkı

Bu iki kavram çok sık karıştırılabilir.

### Iterative

**Aynı ürün üzerinde tekrar tekrar iyileştirme yapılır.**

Örnek:

**Basit çalışan ürün → Daha iyi ürün → Daha gelişmiş ürün**

### Incremental

**Ürün parçalara bölünerek tamamlanır.**

Örnek:

**Parça 1 → Parça 2 → Parça 3 → Tam ürün**

### Akılda tutmak için:

> **Iterative = Aynı şeyi geliştirerek tekrar tekrar iyileştirmek**

> **Incremental = Ürüne parça parça yeni bölümler eklemek**

---

# 11. Resim Örneğiyle Fark

Bir resim çizdiğimizi düşünelim.

### Iterative yaklaşım

Önce basit bir çizim yaparız.

Sonra:

* Detay ekleriz.
* Renk ekleriz.
* Gölge ekleriz.
* Gerçekçiliği artırırız.

İlk versiyon kullanılabilir bir fikir sunabilir ve her iterasyonda daha iyi hale gelir.

### Incremental yaklaşım

Resmin bir bölümünü tamamen tamamlarız.

Sonra başka bir bölümünü tamamlarız.

Sonra diğer bölümü tamamlarız.

En sonunda bütün resim ortaya çıkar.

İlk aşamalarda ortaya çıkan parça tek başına anlamlı veya kullanılabilir olmayabilir.

---

# 12. Agile'ın Önemli Avantajı

Agile yaklaşımında müşteri daha erken geri bildirim verebilir.

Örneğin ilk versiyonu gördüğünde:

> "Ben aslında bunu böyle istememiştim."

diyebilir.

Ekip bu geri bildirimi sonraki iterasyonda dikkate alabilir.

Bu, büyük projenin sonunda yanlış ürünü ortaya çıkarma riskini azaltabilir.

Aynı zamanda:

* Zaman kaybını,
* Gereksiz geliştirmeyi,
* Maliyeti,
* Yanlış ürünü geliştirme riskini

azaltmaya yardımcı olabilir.

---

# 13. QA / Test Uzmanı Açısından Neden Önemli?

Bir test uzmanı için SDLC'yi bilmek çok önemlidir.

Çünkü test uzmanı:

* Gereksinimleri analiz eder.
* Testleri planlar.
* Test senaryoları oluşturur.
* Gereksinimlerin test edilebilirliğini değerlendirir.
* Testleri gerçekleştirir.
* Hataları raporlar.
* Düzeltmeleri retest eder.
* Gerektiğinde regresyon testi yapar.
* Geliştirme ekibi ve Product Owner/Business Analyst ile iletişim kurar.

Ve en önemlisi:

> **Test sadece geliştirme bittikten sonra yapılan bir işlem değildir.**

Test düşüncesi projenin erken aşamalarında başlamalıdır.

---

# 14. QA Perspektifinden Benim Çıkardığım Sonuç

SDLC'yi öğrenirken benim için en önemli fikir şudur:

**Test uzmanı projenin sonunda ortaya çıkan ürünü kontrol eden kişi değildir.**

Test uzmanı mümkün olduğunca erken aşamadan sürece dahil olur.

Örneğin gereksinim aşamasında:

> "Bu gereksinim açık mı?"

> "Test edilebilir mi?"

> "Burada eksik veya çelişkili bir durum var mı?"

diye düşünür.

Daha sonra tasarım, geliştirme ve test aşamalarında sürece devam eder.

Bu nedenle kaliteli yazılım üretmek için **testi sona bırakmak yerine kaliteyi sürecin tamamına yaymak** gerekir.

---

#  Akılda Tutmam Gereken Kavramlar

| Kavram              | Kısa Anlamı                                                          |
| ------------------- | -------------------------------------------------------------------- |
| **SDLC**            | Yazılım geliştirme yaşam döngüsü                                     |
| **Sequential**      | Aşamaların sırayla ilerlemesi                                        |
| **Waterfall**       | Sıralı/şelale geliştirme modeli                                      |
| **Early Testing**   | Test faaliyetlerinin erken başlaması                                 |
| **V-Model**         | Geliştirme aşamalarını test seviyeleriyle eşleştiren model           |
| **Agile**           | Küçük parçalar halinde, sürekli geri bildirimle geliştirme yaklaşımı |
| **Iterative**       | Ürünü tekrar tekrar geliştirerek iyileştirme                         |
| **Incremental**     | Ürünü parçalar halinde oluşturma                                     |
| **Sprint**          | Agile'da belirli süreli çalışma döngüsü                              |
| **Retest**          | Düzeltilen hatanın tekrar test edilmesi                              |
| **Regression Test** | Değişikliklerin mevcut özellikleri bozup bozmadığını kontrol etmek   |

##  Tek cümlelik özet

> **SDLC, yazılımın gereksinimlerden başlayarak tasarım, geliştirme, test, yayınlama ve bakım aşamalarından geçmesini tanımlar; bir test uzmanı için en önemli nokta ise test faaliyetlerinin yalnızca geliştirme sonunda değil, mümkün olduğunca erken başlamasıdır.**
