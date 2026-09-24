# Clomosy TRObject Code Samples & Best Practices

[![Platform](https://img.shields.io/badge/Platform-Clomosy-orange.svg)](https://clomosy.com)
[![Language](https://img.shields.io/badge/Language-TRObject-blue.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Bu depo, **Clomosy** mobil uygulama geliştirme platformunda **TRObject** programlama dili ile geliştirilmiş kurumsal kod kalıplarını, donanım entegrasyonlarını, yerel veritabanı mimarilerini ve REST API çözümlerini içerir.

---

## 📌 Modül ve Örnek Kataloğu

| Modül / Dizin | Kapsam | Öne Çıkan Özellikler | Durum |
| :--- | :--- | :--- | :---: |
| [📍 Canlı Hava & GPS (Leaflet)](./02-data-and-sensors/live-weather-gps-rest/) | Veri & Sensör Entegrasyonu | `TclRest`, Open-Meteo API, GPS Timer, Leaflet JS WebView | ✅ Hazır |
| [📈 Kurumsal CRM & Dashboard](./04-complete-apps/enterprise-crm-dashboard/) | Uçtan Uca Tam Uygulama | Yerel SQLite CRUD, Canlı KPI & Çubuk Grafik, Accordion UI | ✅ Hazır |
| `01-ui-components` | Dinamik Arayüz Tasarımı | Dynamic Layout, Form Kontrolleri, Özel Kart Bileşenleri | ⏳ Planlandı |
| `03-hardware-and-sensors` | Donanım ve Servisler | Barkod / QR Okuma, Kamera, Push Notification | ⏳ Planlandı |

---

## 🚀 Başlarken

### Gereksinimler
- **Clomosy App** (iOS / Android) mobil test ortamı
- **Clomosy Web IDE** veya masaüstü geliştirme ortamı

### Kodları Çalıştırma
1. İlgili modül klasöründeki `.tro` uzantılı kaynak kodu kopyalayın.
2. Clomosy IDE üzerinde yeni bir proje açıp kod editörüne yapıştırın.
3. Clomosy mobil uygulaması üzerinden projeyi anında test edin.

---

## 💡 Kodlama Standartları
- **Veritabanı Dayanıklılığı:** Tablo yapıları ve sütun güncellemeleri migrasyon kontrolleriyle (`IF NOT EXISTS`, `ALTER TABLE`) desteklenir.
- **Hata Toleransı:** Mobil cihazların bölgesel ayarlarından doğabilecek koordinat/ondalık uyuşmazlıkları (`,`/`.`) normalize edilmiştir.
- **Performans & Temizlik:** Dinamik arayüzlerde bileşen bellek yönetimi (`Free` çağrıları) gözetilmiştir.

---

## 📄 Lisans
Bu proje [MIT Lisansı](LICENSE) altında açık kaynak olarak paylaşılmaktadır.
