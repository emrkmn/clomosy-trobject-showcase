# 🚗 Car Wash & Auto Detailing Service Tracker

Clomosy platformunda **TRObject** dili ile geliştirilmiş; oto yıkama, oto kuaför ve servis işletmeleri için anlık operasyon takibi, dinamik ciro analizi ve müşteri kabul süreçlerini yöneten hafif ve güçlü bir **Hizmet & Servis Takip Uygulaması**.

---

## 🌟 Öne Çıkan Mimari Özellikler

- **Canlı KPI ve Günlük Ciro Takibi:** Bekleyen araç sayısı, teslim edilen araçlar ve bugünün tarihine (`SUBSTR(TeslimTarihi, 1, 10)`) göre dinamik hesaplanan ciro paneli.
- **Dinamik Hizmet/Paket Seçimi (Chip Buttons):** Dış Yıkama, İç+Dış ve Seramik Kaplama paketleri arasında tek tıkla fiyat ve hizmet ataması.
- **Çift Sekmeli Akıcı Geçiş (Tab Indicators):** Araç Kabul (Yeni Kayıt) ve Liste görünümü arasında alt panel sekme göstergeleriyle yumuşak navigasyon.
- **Akıllı Veritabanı Migrasyonu:** `pragma_table_info` sorgusu ile SQLite şemasını kontrol eden ve eksik sütunları (`TeslimTarihi`) otomatik ekleyen dinamik `ALTER TABLE` desteği.
- **Platforma Duyarlı Onay Pencereleri:** Mobil ortamda `Clomosy.AskAndCall`, masaüstünde `Clomosy.Ask` kullanarak platformlar arası hatasız teslim/silme onayı.

---

## 🛠️ Kullanılan Clomosy Sınıfları & Bileşenler

| Bileşen / Sınıf | Kullanım Amacı |
| :--- | :--- |
| `TclSQLiteQuery` | İş emri ekleme, durum güncelleme (`Durum = 1`), teslim tarihi mühürleme ve canlı ciro sorguları |
| `TclProPanel` & `TclProButton` | Modern kart tasarımları, durum renk barları (Sarı: Bekliyor, Yeşil: Teslim) ve filtre çipleri |
| `TclProSearchEdit` | Anlık plaka bazlı arama ve filtreleme |
| `TclVertScrollBox` | Dinamik olarak üretilen iş kartlarının kaydırılabilir listesi |
| `TclLayout` | Yan yana form alanları (Model ve Telefon) için responsive yerleşim |

---

## 🚀 Çalıştırma

1. `App.tro` dosyasındaki kodları kopyalayın.
2. Clomosy IDE'de yeni bir proje açarak kod editörüne yapıştırın.
3. Test simülatöründe veya fiziksel cihazınızda projeyi çalıştırın.
4. İlk çalıştırmada `CarWashV6.db` veritabanı ve `TBL_JOBS` tablosu otomatik oluşturulacaktır.
