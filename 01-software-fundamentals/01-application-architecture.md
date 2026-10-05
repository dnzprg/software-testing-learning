# Tek Katmanlı ve Çok Katmanlı Uygulamalar

## 1. Tek Katmanlı Uygulamalar

Tek katmanlı uygulamalarda kullanıcı arayüzü, iş mantığı ve veri aynı uygulama içerisinde bulunur.

### Özellikleri

* Basit bir mimariye sahiptir.
* Geliştirilmesi kolaydır.
* Test edilmesi daha kolaydır.
* Genellikle sunucu veya internet bağlantısı gerektirmez.
* Hataların kaynağını bulmak daha kolaydır.

### Örnekler

* Hesap makinesi
* Çevrimdışı yapılacaklar listesi
* Basit masaüstü uygulamaları
* Alarm uygulaması

---

## 2. Çok Katmanlı Uygulamalar

Modern web ve mobil uygulamaların çoğu çok katmanlı mimariye sahiptir. Uygulamanın farklı sorumlulukları farklı katmanlara ayrılır.

### Temel Katmanlar

#### Presentation Layer – Sunum Katmanı

Kullanıcının gördüğü ve etkileşim kurduğu bölümdür.

Örnek:

* Login ekranı
* Butonlar
* Formlar
* Menü ve sayfalar

#### Business Layer – İş Katmanı

Uygulamanın kurallarını ve iş mantığını içerir.

Örnek:

* Kullanıcı giriş yaptığında hangi sayfaya yönlendirileceği
* Öğrencinin hangi işlemleri yapabileceği
* Sepete ürün eklendiğinde hangi işlemlerin gerçekleşeceği

#### Data Layer – Veri Katmanı

Uygulamanın verilerinin saklandığı ve yönetildiği bölümdür.

Örnek:

* Kullanıcı bilgileri
* Ürün bilgileri
* Siparişler
* Veritabanı

---

## 3. Login Örneği

Bir kullanıcı sisteme giriş yaptığında genel olarak şu süreç gerçekleşebilir:

**Kullanıcı → Sunum Katmanı → İş Katmanı → Veri Katmanı → İş Katmanı → Sunum Katmanı → Kullanıcı**

Kullanıcı adı ve şifre gönderilir. Sistem bilgileri kontrol eder ve sonucu kullanıcıya gösterir.

---

## 4. Test Açısından Neden Önemli?

Bir test uzmanı için çok katmanlı mimariyi anlamak önemlidir. Çünkü karşılaşılan bir hatanın kaynağı her zaman kullanıcının gördüğü ekran olmayabilir.

### Örnekler

**Sunum katmanı hatası:**
Login butonuna tıklıyorum ancak hiçbir işlem gerçekleşmiyor.

**İş katmanı hatası:**
Öğrenci hesabıyla giriş yapan kullanıcı öğretmen profiline yönlendiriliyor.

**Veri katmanı hatası:**
Doğru kullanıcı adı ve şifre girildiği halde sistem kullanıcı bilgilerini veritabanından yanlış okuyor.

Bu nedenle bir test uzmanı hata ile karşılaştığında yalnızca "ekranda ne oluyor?" sorusuna değil, problemin hangi katmandan kaynaklanabileceğine de bakmalıdır.

## 5. Test Uzmanı İçin Öğrenilmesi Gereken Ana Nokta

> Bir uygulamada görülen hata, mutlaka kullanıcı arayüzünden kaynaklanmaz. Problem sunum, iş mantığı veya veri katmanında olabilir.


