# 💰 Telegram Finans Botu

Kişisel gelir ve giderlerinizi kolayca takip edebileceğiniz, canlı döviz kurlarını görüntüleyebileceğiniz ve aylık finansal raporlar oluşturabileceğiniz gelişmiş bir Telegram botu.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Database](https://img.shields.io/badge/Database-SQLite-orange)

## ✨ Özellikler

- 📊 **Gelir/Gider Takibi:** Adım adım sihirbaz ile hızlıca işlem kaydetme.
- 💱 **Canlı Kurlar:** TCMB üzerinden Dolar, Euro, Sterlin ve uluslararası piyasadan Ons Altın verileri ile Gram Altın hesaplama.
- 📂 **Kategori Yönetimi:** Gelir ve Giderler için özel ayrılmış kategori listeleri.
- 📈 **Aylık Özet & Excel:** Ay sonunda detaylı karşılaştırmalı analiz içeren Excel dosyası indirme.
- 🔍 **Akıllı Arama:** Kategoriye göre harcama detaylarını görüntüleme.
- 📅 **Haftalık Rapor:** Son 7 günün harcama özeti ve finansal ipuçları.
- 🖊️ **İşlem Yönetimi:** Eklenen işlemleri düzenleme veya silme.
- 🔔 **Akıllı Bildirimler:** Pozitif/Negatif bakiye durumuna göre motive edici mesajlar.

## 🚀 Komutlar

| Komut | Açıklama |
| :--- | :--- |
| `/start` | Botu başlat ve yardım menüsünü gör |
| `/ekle` | Yeni gelir veya gider ekle |
| `/bakiye` | Toplam gelir, gider ve net durumu gör |
| `/kur` | Güncel döviz ve altın kurlarını getir |
| `/haftalik` | Son 7 günün harcama özetini gör |
| `/listele` | Son 5 işlemini listele |
| `/ara` | Kategori bazlı harcama detaylarını gör |
| `/duzenle <id>` | Bir işlemi güncelle |
| `/sil <id>` | Bir işlemi sil |
| `/aylik_ozet` | Aylık karşılaştırmalı Excel raporunu indir |
| `/yardim` | Yardım menüsünü tekrar getir |
| `/iptal` | Aktif işlemi iptal et |

## 🛠️ Kurulum (Lokal)

Projeyi kendi bilgisayarınızda çalıştırmak için şu adımları izleyin:

1. **Repo'yu İndirin:**
   ```bash
   git clone https://github.com/kullanici-adiniz/repo-adi.git
   cd repo-adi
   ```

2. **Gerekli Kütüphaneleri Yükleyin:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Ortam Değişkenlerini Ayarlayın:**
   Proje kök dizininde `.env` adında bir dosya oluşturun ve bot token'ınızı ekleyin:
   ```env
   TELEGRAM_BOT_TOKEN=your_bot_token_here
   ```

4. **Botu Başlatın:**
   ```bash
   python bot.py
   ```

## ☁️ Sunucu Dağıtımı (Railway / Heroku / VPS)

Bu proje bulut ortamlarında 7/24 çalışmak üzere tasarlanmıştır.
- **Railway:** Depoyu bağlayın, `TELEGRAM_BOT_TOKEN` değişkenini ekleyin ve başlatın. Veritabanının kaybolmaması için **Volume** eklemeyi unutmayın.
- **VPS:** Bir Python ortamı kurup `nohup python bot.py &` komutu ile arka planda çalıştırabilirsiniz.

## 📂 Proje Yapısı

```
.
├── bot.py              # Ana bot kodu ve komutlar
├── data.db             # SQLite veritabanı (Otomatik oluşturulur)
├── requirements.txt    # Python bağımlılıkları
├── .env                # API Anahtarları (Güvende tutun!)
└── README.md           # Dokümantasyon
```

## 📜 Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.
