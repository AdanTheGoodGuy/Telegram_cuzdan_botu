# 📊 Telegram Finans Botu - Proje Raporu

## 🎯 Proje Amacı
Kişisel finans yönetimini kolaylaştırmak, gelir-gider takibini dijitalleştirmek ve kullanıcılara aylık finansal analizler sunmak amacıyla geliştirilmiş bir Telegram botudur.

## 🛠️ Yapılan İşlemler ve Süreç

### 1. Temel Özellikler (Core Features)
- **Gelir/Gider Yönetimi:** 
  - `/ekle` komutu ile adım adım gelir/gider kaydı
  - Kategorizasyon: Gelir (Maaş, Freelance, Yatırım Getirisi vb.) ve Gider (Market, Fatura, Ulaşım vb.) için ayrılmış kategoriler
  - `/duzenle <id>` ile mevcut işlemleri güncelleme
  - `/sil <id>` ile işlem silme

- **Finansal Analizler:**
  - `/bakiye`: Anlık net bakiye hesaplama (Gelir - Gider)
  - `/haftalik`: Son 7 günün harcama özeti + finansal ipuçları
  - `/listele`: Son 5 işlemi görüntüleme
  - `/ara`: Kategori bazlı harcama detaylarını listeleme

### 2. Gelişmiş Raporlama (Advanced Reporting)
- **`/aylik_ozet` Komutu:**
  - Aylık gelir/gider karşılaştırması
  - Önceki ay ile % değişim analizi
  - Kategori bazlı gider dağılımı
  - Excel formatında indirilebilir rapor (openpyxl ile oluşturulur)
  - İçgörüler: "Bu ay yemeye geçen aya göre %20 daha fazla harcadın" gibi

### 3. Canlı Veri Entegrasyonu
- **`/kur` Komutu:**
  - TCMB günlük döviz kurları (XML parse)
  - Gram Altın hesaplama: `(Ons Altın USD × TCMB USD/TRY) / 31.1035`
  - vang.today API üzerinden XAU/USD verisi

### 4. Kullanıcı Deneyimi (UX Improvements)
- **Emoji Desteği:** Tüm komutlarda görsel iyileştirme (💰, 💸, 📊 vb.)
- **Mesajlar:** 
  - 8 farklı gelir mesajı
  - 8 farklı gider mesajı
  - 6 pozitif/negatif bakiye uyarısı
  - 10 finansal ipucu
- **Hata Yönetimi:** `/iptal` komutu ile işlem iptali, ConversationHandler fallback desteği
- **Yardımcı Fonksiyonlar:** `edit_menu_keyboard()`, `category_buttons()` ile kod tekrarının önlenmesi

### 5. Deployment ve Güvenlik
- **Railway Deployment:** 7/24 bulut tabanlı çalışma
- **Volume Entegrasyonu:** SQLite veritabanının (`data.db`) kalıcı hale getirilmesi
- **MIT Lisansı:** Açık kaynak lisansı eklenmesi
- **`.env` ve `data.db` koruma:** `.gitignore` ile gizlilik

## 📈 Sonuçlar

### Teknik Başarılar
✅ **SQLite Entegrasyonu:** Hafif, sunucusuz veritabanı ile verimli veri saklama
✅ **Telegram Bot API:** `python-telegram-bot` kütüphanesi ile stabil iletişim
✅ **Excel Raporlama:** `openpyxl` ile profesyonel görünümlü raporlar
✅ **XML/JSON Parse:** TCMB ve vang.today API'lerinden veri çekme
✅ **ConversationHandler:** Çok adımlı sohbet akışlarının yönetimi

### Kullanıcı Deneyimi
✅ **Sezgisel Arayüz:** Emojiler ve açıklayıcı metinlerle kullanıcı dostu deneyim
✅ **Akıllı Analizler:** Aylık karşılaştırmalar ve finansal ipuçları
✅ **Esneklik:** Gelir ve giderler için özelleştirilmiş kategoriler

## 🚀 Gelecek Önerileri

1. **Grafiksel Raporlar:** Excel raporuna pasta grafiği ve trend çizgileri eklenmesi
2. **Düzenli Hatırlatıcılar:** Her ayın 1'inde bakiye özeti gönderme (APScheduler)
3. **Çoklu Para Birimi:** Dolar/Euro cinsinden gelir/gider takibi
4. **Hedef Yönetimi:** Belirli bir hedefe (örn: Araba, Tatil) para biriktirme modülü
5. **Güvenlik:** Kullanıcı bazlı şifreleme veya 2FA desteği

## 📂 Proje Yapısı
```
bot_finans/
├── bot.py              # Ana bot kodu (~680 satır)
├── data.db             # SQLite veritabanı
├── requirements.txt    # Bağımlılıklar
├── .env                # API anahtarları (güvende)
├── LICENSE            # MIT Lisansı
├── README.md           # Proje dokümantasyonu
└── PROJE_RAPORU.md    # Bu rapor
```

## 🎉 Sonuç
Proje başarıyla tamamlanmış, Railway bulut platformunda 7/24 hizmet vermeye hazır hale getirilmiştir. Kullanıcılar Telegram üzerinden finansal işlemlerini yönetebilmekte, aylık raporlar alabilmekte ve finansal okuryazarlıklarını artıracak ipuçları edinebilmektedir.

---
*Tarih: Mayıs 2026*
*Geliştirici: AdanTheGoodGuy*
