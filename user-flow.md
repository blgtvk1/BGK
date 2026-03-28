# 🗺️ LexiaBuddy: Kullanıcı Akışı (User Flow)

Bu doküman, bir kullanıcının uygulamayı açtığı andan materyali aldığı ana kadar geçen adımları tanımlar.

---

### 🟢 Adım 1: Karşılama ve Profil Seçimi
* **Ekran:** `Giriş / Profil Seçim Ekranı`
* **Kullanıcı Eylemi:** Mevcut bir öğrenci profilini seçer veya yeni profil oluşturur.
* **Sistem:** Öğrencinin disleksi seviyesini (Hafif/İleri) ve font tercihlerini yükler.

### 📸 Adım 2: Materyal Girişi (Giriş Katmanı)
* **Ekran:** `Yükleme / Tarama Ekranı`
* **Kullanıcı Eylemi:** * Kamerayı açıp kitap sayfasının fotoğrafını çeker.
    * VEYA cihazdan bir PDF/Görsel dosyası yükler.
* **Sistem:** OCR (Görüntü İşleme) motorunu başlatır ve metni dijitalleştirir.

### ⚙️ Adım 3: Kişiselleştirme (İşlem Katmanı)
* **Ekran:** `Düzenleme Paneli`
* **Kullanıcı Eylemi:** * "Heceleri Renklendir" anahtarını açar.
    * "Metni Sadeleştir" seçeneğini aktif eder.
    * "Zihin Haritası Oluştur" butonuna tıklar.
* **Sistem:** Yapay zeka (GPT-4o) ile metni basitleştirir ve heceleme algoritmasını çalıştırır.

### 🏁 Adım 4: Etkileşimli Okuma ve Çıktı
* **Ekran:** `Sonuç / Okuma Ekranı`
* **Kullanıcı Eylemi:** * Metni OpenDyslexic fontuyla okur.
    * Sesli dinleme (TTS) ikonuna basar.
    * "PDF Olarak İndir" butonuna basarak çıktısını alır.
* **Sonuç:** Çocuk için optimize edilmiş, basılabilir eğitim materyali hazırdır.

---

## 📈 Akış Diyagramı (Özet)
`Giriş` ➔ `Fotoğraf Çek/Yükle` ➔ `AI İşleme (Sadeleştir + Renklendir)` ➔ `Okuma & PDF Çıktısı`
