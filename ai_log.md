bu dosyaya web projesi dersi boyumca hafta hafta yapay zekaya yazdığımız promtları ve bize verdiği cevapları ve bu cevaplardan nasıl faydalandığımızı not edeceğiz.
16 ekim görevi
ai a sorduğum soru:
verdiği cevap:
ve bu cevabı nasıl kullandım:


KampüsEtkinlik — Üniversite Etkinlik Platformu Proje ve Geliştirme Raporu
Tarih: 14 Ekim 2026
Proje Adı: KampüsEtkinlik
Referans Analiz: Go Campus Case Study (DataHex)
1. Proje Özeti ve Vizyonu
KampüsEtkinlik, üniversite kampüsündeki kulüp faaliyetlerini, akademik ve sosyal atölyeleri, spor turnuvalarını ve festival/konser gibi toplu organizasyonları tek bir çatı altında toplayan dinamik bir etkinlik platformudur.
Platformun temel amacı:
Öğrenciler İçin: Kampüsteki tüm sosyal ve akademik fırsatlardan anında haberdar olmak, ilgi alanlarına göre (Teknoloji, Kültür & Sanat, Spor vb.) filtreleme yapmak ve katılmak istedikleri etkinlikleri kişisel listelerine ekleyerek takip etmek.
Kulüpler ve Organizatörler İçin: Etkinlik duyurularını kolayca yayınlamak, katılım sayılarını takip etmek ve hedef öğrenci kitlesine doğrudan ulaşmak.
2. Arayüz Tasarımı ve Kullanıcı Deneyimi (UI/UX)
14 Ekim 2026 tarihi itibarıyla yapılan arayüz analizleri ve "Go Campus" konsept incelemesi doğrultusunda platformun görsel mimarisi şu bileşenlerden oluşmaktadır:
Header (Üst Navigasyon Barı):
Marka Logosu (KampüsEtkinlik)
Ana Menü Linkleri: Etkinlikler, Kategoriler, Kulüpler / Organizatörler, Katılmak İstediklerim (Dinamik sayaçlı)
Aksiyon Butonları: Giriş Yap ve Etkinlik Oluştur (Vurgulu Turuncu Tasarım)
Hero (Karşılama Bölümü):
Dikkat çekici ana başlık ve slogan.
Canlı arama çubuğu (Etkinlik, kulüp veya anahtar kelimeye göre arama).
Kampüs istatistik paneli (Örn: 240+ Yayınlanan Etkinlik, 18K+ Toplam Kayıt, 60+ Aktif Kulüp).
Öne Çıkan Etkinlik Kartı: Yaklaşan en büyük organizasyon için ayrılmış özel renkli (Gradient) alan.
Etkinlik Kataloğu ve Kategoriler:
Kategori Filtre Butonları (Tümü, Teknoloji, Kültür & Sanat, Spor, Atölyeler).
Renkli ve tarih rozetli (Date Badge) modern etkinlik kartları.
Etkinlik bazlı "+ Katılmak İstediklerime Ekle" etkileşim butonu.
3. Teknik Mimari ve Teknoloji Yığını (Tech Stack)
Platformun geliştirilme sürecinde performans, ölçeklenebilirlik ve sürdürülebilirlik göz önüne alınarak Seçenek A (JavaScript / TypeScript Ekosistemi) mimarisi benimsenmiştir:
Katman	Teknoloji / Kütüphane	Kullanım Amacı
Önyüz (Frontend)	React.js / Next.js	Dinamik bileşen yönetimi, hızlı sayfa geçişleri ve güçlü SEO performansı.
Stil & Tasarım	Tailwind CSS	Modern, esnek ve responsive (mobil uyumlu) arayüz kodlaması.
Arka Yüz (Backend)	Node.js (Express) / Supabase	REST API servisleri, yetkilendirme ve veri yönetimi.
Veritabanı	PostgreSQL	Kullanıcı, etkinlik, kulüp ve katılım verilerinin ilişkisel olarak tutulması.
4. Veritabanı Modelleri (Database Schema)
Sistemin arka planında çalışacak temel veritabanı tabloları aşağıda planlanmıştır:
Users (Kullanıcılar): id, ad_soyad, email, sifre_hash, rol (Öğrenci / Kulüp Yöneticisi)
Clubs (Kulüpler): id, kulup_adi, aciklama, logo_url, yonetici_id
Events (Etkinlikler): id, baslik, aciklama, kategori, tarih_saat, konum, kulup_id, kapasite
Favorites / Bookmarks (Katılmak İstediklerim): id, kullanici_id, etkinlik_id, eklenme_tarihi
