# 📦 Retail Inventory & POS Management System

Clomosy platformunda **TRObject** dili ile geliştirilmiş; **4 bağımsız birimden (Unit)** oluşan, yerel SQLite veritabanı destekli, kamera ile barkod okuma yetenekli ve CSV/Fiş paylaşım servislerine sahip uçtan uca bir **Mobil Perakende Stok ve Hızlı Satış (POS) Sistemi**.

---

## 🏗️ Çok Birimli Mimari (Multi-Unit Architecture)

Uygulama modüler mimari prensiplerine uygun olarak `Clomosy.RunUnit` fonksiyonu ile birbirine bağlanan 4 çalışma biriminden oluşur:

| Birim / Dosya | Modül Adı | Temel İşlevler |
| :--- | :--- | :--- |
| **`01-UMain.tro`** | Dashboard & Navigasyon | Dinamik ekran ölçekleme (`CalcScale`), animasyonlu Bottom Sheet menü (`TclTimer`), hızlı modül geçişleri. |
| **`02-UDepo.tro`** | Stok & Depo Yönetimi | SQLite ürün CRUD (Ekle, Güncelle, Sil, Ara), responsive çift panel (Tablet/Telefon), `TclProListViewDesignerPanel` listelemesi. |
| **`03-USatis.tro`** | Hızlı Satış (POS) | Kamera ile canlı barkod okuma (`CallBarcodeReader`), dinamik sepet sepet dizilimi (`TclStringList`), stok kontrolü ve otomatik stok düşümü. |
| **`04-USatisGecmisi.tro`** | Satış Geçmişi & Rapor | Tarih aralığı filtreleme (`TclDateEdit`), detaylı fiş dökümü, TXT fiş paylaşımı ve CSV Excel satış raporu çıktısı (`TclShareService`). |

---

## 🌟 Öne Çıkan Teknik Yetenekler

- **Donanım Barkod Okuyucu:** `SatisForm.CallBarcodeReader` ile mobil cihazın kamerasını doğrudan barkod okuyucu olarak kullanma.
- **Dinamik Fiş ve CSV Dışa Aktarma:** `TclShareService` aracılığıyla satış fişlerini `.txt` ve toplu satış hareketlerini `.csv` dosyası olarak WhatsApp, Mail veya cihaz servislerine aktarma.
- **Otomatik Şema Kurulumu:** SQLite üzerinde `StokTakip` ve `SatisGecmisi` tablolarının varlığını denetleyen ve otomatik oluşturan altyapı.
- **Akıllı Cihaz Duyarlılığı (Responsive Engine):** Ekran genişliğine ve platforma göre dikey kaydırma veya yatay bölünmüş çift panel düzenine anlık geçiş.

---

## 🚀 Çalıştırma Talimatı

1. Clomosy IDE üzerinde projenizi oluşturun.
2. 4 dosyayı aynı proje altına ilgili birim isimleriyle (`UMain`, `UDepo`, `USatis`, `USatisGecmisi`) tanımlayın.
3. Proje başlangıç birimi olarak `UMain` birimini ayarlayın ve derleyin.
