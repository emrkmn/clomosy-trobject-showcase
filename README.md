# Clomosy TRObject Code Samples & Best Practices

[![Platform](https://img.shields.io/badge/Platform-Clomosy-orange.svg)](https://clomosy.com)
[![Language](https://img.shields.io/badge/Language-TRObject-blue.svg)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Bu depo, **Clomosy** mobil uygulama geliştirme platformunda **TRObject** programlama dili ile geliştirilmiş kurumsal kod kalıplarını, donanım entegrasyonlarını ve REST API mimarilerini içerir.

---

## 📌 Modül ve Örnek Kataloğu

| Modül / Dizin | Kapsam | Öne Çıkan Özellikler | Durum |
| :--- | :--- | :--- | :---: |
| [📍 Canlı Hava & GPS (Leaflet)](./02-data-and-sensors/live-weather-gps-rest/) | Veri & Sensör Entegrasyonu | `TclRest`, Open-Meteo API, GPS Timer, Leaflet JS WebView | ✅ Hazır |
| `01-ui-components` | Dinamik Arayüz Tasarımı | Dynamic Layout, Form Kontrolleri, Özelleştirilmiş Bileşenler | ⏳ Planlandı |
| `03-hardware-and-sensors` | Donanım ve Servisler | Barkod / QR Okuma, Kamera, Push Notification | ⏳ Planlandı |
| `04-complete-apps` | Uçtan Uca Mini Uygulamalar | SQLite CRUD, Saha Operasyon & Ziyaret Akışları | ⏳ Planlandı |

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
- **Hata Toleransı:** Mobil cihazların bölgesel ayarlarından doğabilecek koordinat/veri uyuşmazlıkları (örn: `,` / `.` dönüşümleri) ele alınmıştır.
- **Asenkron Güvenlik:** Donanım servisleri (GPS, Kamera) zaman aşımı (timeout) kontrolleriyle donatılmıştır.
- **Modülerlik:** Her örnek bağımsız olarak derlenebilir ve çalıştırılabilir yapıdadır.

---

## 📄 Lisans
Bu proje [MIT Lisansı](LICENSE) altında açık kaynak olarak paylaşılmaktadır.
