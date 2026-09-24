# 📈 Enterprise CRM Portal & Dynamic Sales Dashboard

Bu proje, Clomosy platformunda **TRObject** programlama dili ile geliştirilmiş; yerel veritabanı destekli, canlı analiz ve raporlama yeteneklerine sahip tam kapsamlı bir kurumsal **Mobil Müşteri İlişkileri Yönetimi (CRM)** uygulamasıdır.

---

## 🌟 Öne Çıkan Mimari Özellikler

- **Yerel SQLite CRUD Mimarisi:** Otomatik tablo kurma (`CREATE TABLE IF NOT EXISTS`), şema migrasyonu (`ALTER TABLE`) ve dinamik kayıt filtreleme.
- **Canlı Analitik & Dinamik Çubuk Grafik:** Müşteri ve teklif durumlarına göre gerçek zamanlı ciro, kazanma oranı ve aylık satış grafiği hesaplama.
- **Özel Kart Accordion Arayüzü:** Müşteri kartlarına tıklandığında yumuşak geçişle genişleyen detay paneli, hızlı arama, WhatsApp (`wa.me`), doğrudan telefon arama (`TClomosyOS.Dial`) ve e-posta tetikleyicileri.
- **Responsive Tasarım:** Ekran genişliğine göre (`OnFormResize`) otomatik uyum sağlayan akıllı masaüstü/mobil panel düzeni.
- **Pop-up Modal & Durum Yönetimi:** Katmanlı arayüz (Overlay) ile form doğrulama destekli yeni müşteri ve fırsat ekleme akışı.

---

## 🛠️ Kullanılan Clomosy Bileşenleri & Sınıfları

| Bileşen / Sınıf | İşlev |
| :--- | :--- |
| `TClSQLiteQuery` | SQLite üzerinde okuma, yazma, güncelleme ve toplu istatistik sorguları |
| `TclProPanel` & `TclProLabel` | Kurumsal Dark/Light UI kartları ve durum hapları (Status Pills) |
| `TclHorzScrollBox` / `TclVertScrollBox` | Yatay KPI kart kaydırma ve dikey aktivite/müşteri listeleri |
| `TclProEdit` | Canlı arama ve modal form giriş alanları |
| `TClomosyOS` | Cihazın telefon arama, WhatsApp URL şeması ve e-posta servislerini tetikleme |

---

## 🚀 Nasıl Çalıştırılır?

1. `App.tro` dosyasındaki kod bloğunu kopyalayın.
2. Clomosy IDE üzerinde yeni bir projeye yapıştırın.
3. Test emülatöründe veya fiziksel cihazınızda (Clomosy App) projeyi derleyip çalıştırın.
4. İlk açılışta veritabanı otomatik olarak oluşturulacak ve örnek demo veriler yüklenecektir.
