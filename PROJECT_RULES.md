# Klise Ortaklik Takip Sistemi - Kapsamli Proje Ozeti

## Proje Tanimi
NAS tabanli, PocketBase backend kullanan modern web uygulamasi. Apple tarzi glassmorphism tasarimla klise verilerini yonetmek, takip etmek ve coklu kullanici ortaminda paylasmak icin gelistirildi.

## Mevcut Kod ve Versiyon Kontrolu
GitHub Repository: https://github.com/RealX11/klise-takip-sistemi
Raw HTML URL: https://raw.githubusercontent.com/RealX11/klise-takip-sistemi/refs/heads/main/index.html
Live Demo URL: https://realx11.github.io/klise-takip-sistemi/
Mevcut Versiyon: V1 (4 Eylul 2025, 14:30)

## Teknik Altyapi
Backend: PocketBase (Go tabanli, SQLite embedded)
Veritabani: SQLite (NAS'ta kalici depolama)
Real-time: PocketBase WebSocket baglantisi
Hosting: NAS Docker environment
Versiyonlama: Git (GitHub)

## Sistem Gereksinimleri
NAS IP: 192.168.2.30
PocketBase Port: 8090
Web Erisim: http://192.168.2.30:8090/
Admin Panel: http://192.168.2.30:8090/_/
Dosya Konumu: /docker/data/pb_public/index.html

## Bekleyen Gelistirmeler
Role-Based Access Control (Oncelikli)
- Admin Kullanicilar: Muge, Buket, Selin (tam yetki)
- Viewer Kullanici: Murat (sadece goruntuleme)

## Teknik Referanslar
PocketBase API Rules Dokumantasyonu: https://pocketbase.io/docs/
Ozellikle: Filter syntax kurallari, Authentication kontrolu, Role-based access control ornekleri

NAS Docker Environment: Proje gorsellerinde NAS yapilandirmasi, klasor yapisi ve Docker container ayarlari referans alinacak.

## Veritabani Semasi
Kliseler Collection: kliseKodu, bicakOlcusu, kliseTuru (Emboss/Lak), isKodlari (JSON array), aciklama
Users Collection: email, password, name, role (admin/viewer - YENİ EKLENEN)

SONRAKI ÖZELLIK: Eylem geçmişi sistemi
- PocketBase'de Eylem_Penceresi collection'ı oluşturuldu
- Her klişe işleminde otomatik log kaydı 
- İki görünüm: klişe bazında + global sistem logu
