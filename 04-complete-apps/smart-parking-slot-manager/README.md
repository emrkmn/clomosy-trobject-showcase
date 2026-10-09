# 🅿️ Smart Parking Slot & Fee Management System

Clomosy platformunda **TRObject** programlama dili ile geliştirilmiş; 20 araçlık sabit kapasiteli otoparklarda slot durumlarını görselleştiren, dakika bazlı dinamik ücret hesaplayan ve çıkış/tahsilat geçmişini raporlayan **Akıllı Otopark ve Ücret Yönetim Uygulaması**.

---

## 🌟 Öne Çıkan Mimari Özellikler

- **Dinamik 4x5 Slot Matrisi (Grid Calculation):** Ekran genişliğini matematiksel olarak 4 eşit sütuna bölen, slot durumuna göre anlık Yeşil (BOŞ) / Kırmızı (DOLU + Plaka) kartları çizen dinamik arayüz motoru.
- **Süre ve Tarife Hesaplama Motoru:**
  - Giriş zamanı ile çıkış zamanı arasındaki farkı dakika hassasiyetinde hesaplar (`(Now - GirisZamani) * 1440`).
  - Araç tipine göre katsayı uygular (Otomobil 1.0x, Kamyon/TIR 2.0x).
  - Minimum taban ücret (`MIN_FEE`) kontrolü ile kısa süreli parklar için emniyet barajı sağlar.
- **Modal Tabanlı Giriş/Çıkış Akışı:** Ayrı ekranlara gitmeden, tek bir overlay modal üzerinden plaka girişi, araç tipi seçimi veya çıkış/tahsilat onayı alma.
- **Canlı Doluluk & Ciro Takibi:** `COUNT` ve `SUM` sorguları ile anlık Dolu/Boş slot sayıları ve toplam otopark cirosu.
- **Geçmiş & İşlem Dökümü:** `TBL_HISTORY` tablosundan son hareketleri araç ikonları (🚗 / 🚛), park süresi ve tahsilat tutarıyla dikey akışta listeleme.

---

## 🛠️ Kullanılan Clomosy Sınıfları & Bileşenler

| Bileşen / Sınıf | Kullanım Amacı |
| :--- | :--- |
| `TclSQLiteQuery` | Slot durumu güncelleme (`UPDATE TBL_SLOTS`), geçmiş arşivi (`TBL_HISTORY`) ve ciro toplamları |
| `TclProButton` & `TclProPanel` | Matris slot butonları, modal diyalog kutuları ve alt sekme çubuğu |
| `TclVertScrollBox` | Dinamik slot ızgarası ve işlem geçmişi için dikey kaydırma alanı |
| `TclProEdit` | Büyük harf destekli plaka giriş alanı |
| `Clomosy.Ask` | Çıkış anında süre ve tutar bilgilerini gösteren onay penceresi |

---

## 🚀 Çalıştırma

1. `App.tro` dosyasındaki kod bloğunu kopyalayın.
2. Clomosy IDE üzerinde yeni bir projeye yapıştırın.
3. Test simülatöründe veya fiziksel cihazınızda projeyi çalıştırın.
4. İlk açılışta `ModernParkV1.db` veritabanı kurulacak ve 20 slot otomatik olarak "BOŞ" statüsünde hazır hale getirilecektir.
