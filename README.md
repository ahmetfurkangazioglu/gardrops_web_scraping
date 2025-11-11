# Gardrops Web Scraping Projesi

Gardrops.com'dan çanta kategorisindeki ürün bilgilerini çeken Python web scraping projesi.

## 🎯 Özellikler

- 50 sayfa üzerinden 3,500+ ürün verisi çekme
- Selenium ile dinamik içerik yönetimi
- 13 farklı ürün özelliğini toplama:
  - Ürün Adı, Fiyat, Marka
  - Kategori, Kullanım Durumu, Renk
  - İlan Tarihi, Açıklama
  - Satıcı Bilgisi, Görsel URL
  - Beğeni ve Görüntülenme Sayısı

## 📦 Gereksinimler

```bash
pip install selenium beautifulsoup4 pandas openpyxl
```

## 🚀 Kullanım

1. Jupyter Notebook'u açın
2. Tüm hücreleri sırayla çalıştırın
3. `scrape_gardrops_with_selenium()` fonksiyonunu istediğiniz parametrelerle kullanın
4. Sonuçlar otomatik olarak Excel dosyasına kaydedilir

## 📊 Örnek Çıktı

- **Format:** Excel (.xlsx)
- **Dosya adı:** `gardrops_cantalar_[SAYFA_SAYISI]_SAYFA_[TARIH].xlsx`
- **Örnek:** 3,574 ürün, 144 marka, 11 kategori

## ⚙️ Ayarlar

- `max_pages`: Kaç sayfa scraping yapılacak (varsayılan: 50)
- `max_products_per_page`: Sayfa başına maksimum ürün (varsayılan: tümü)

## 📝 Notlar

- Selenium ChromeDriver kullanır (headless mod)
- Rate limiting için ürünler arası 1 saniye bekleme
- Sayfa yüklemeleri için 3 saniye render süresi

## 🛠️ Teknik Detaylar

- **Next.js** tabanlı site için özel regex parsing
- Escaped JSON formatından veri çıkarma
- Lazy loading için otomatik scroll
- Hata yönetimi ve loglama

## 📄 Lisans

Bu proje kişisel kullanım içindir.
