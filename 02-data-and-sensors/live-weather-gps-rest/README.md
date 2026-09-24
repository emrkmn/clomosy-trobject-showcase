# 📍 Live GPS, Open-Meteo REST API & Dynamic Leaflet Map

Bu modül, Clomosy platformunda **TRObject** dili ile yerel donanım sensörlerinin (GPS), ağ servislerinin (`TclRest`) ve modern web arayüzlerinin (`TCLProWebBrowser` + Leaflet.js) nasıl entegre çalıştığını gösteren uçtan uca bir uygulamadır.

---

## 🌟 Öne Çıkan Özellikler

- **Donanım GPS Erişimi & Zaman Aşımı Kontrolü:** `Clomosy.GetCurrentLocation` ile konum tetiklenir, `TClTimer` yardımıyla uydu sinyali güvenli bir şekilde (20 saniye emniyet süresiyle) beklenir.
- **Bölgesel Koordinat Normalizasyonu:** Mobil cihaz işletim sisteminden virgülle (`,`) gelebilecek koordinatları noktaya (`.`) çevirerek Leaflet ve REST servisinin bozulmasını önler.
- **Canlı REST API (Open-Meteo):** Enlem/boylam bilgisiyle anlık sıcaklık, rüzgar hızı ve hava kodu değerlerini çeker.
- **WMO Standart Kod Eşleme:** Sayısal hava durumu kodlarını kullanıcı dostu simge ve açıklamalara dönüştürür.
- **Dinamik Leaflet / OpenStreetMap Render:** Alınan konum ve hava durumu bilgilerini HTML/JS şablonuna gömerek harita üzerinde canlı işaretçi (marker) ve etki alanı çemberi çizer.

---

## 🛠️ Kullanılan Clomosy Sınıfları & Bileşenler

| Bileşen / Sınıf | İşlev |
| :--- | :--- |
| `TclRest` | Open-Meteo REST API endpoint'ine HTTP GET isteği gönderme |
| `Clomosy.LocationValue` | Cihazın canlı GPS koordinatlarını okuma |
| `Clomosy.ClParseJSON` | REST JSON cevabından sıcaklık ve rüzgar verilerini ayrıştırma |
| `TCLProWebBrowser` | Harita arayüzünü (Leaflet.js) uygulama içinde render etme |
| `TclProPanel` & `TclProLabel` | Bilgi kartları ve durum mesajları için modern arayüz |
| `TClTimer` | Arka planda asenkron GPS sinyal takibi |

---

## 🚀 Nasıl Çalıştırılır?

1. `WeatherGpsRest.tro` dosyasındaki kod bloğunu kopyalayın.
2. Clomosy Web IDE veya Clomosy ortamında yeni bir projeye yapıştırın.
3. Mobil cihazınızda (Clomosy App) projeyi çalıştırın.
4. Cihazınızın konum iznini onaylayıp **"📍 Konumu Al"** butonuna dokunun.
