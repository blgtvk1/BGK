# 📄 Ürün Gereksinim Dokümanı (PRD): LexiaBuddy

**Proje Sahibi:** Bilge Tavukçuoğlu (Full Stack Developer & PDR Uzmanı Adayı)  
**Sürüm:** 1.0  
**Tarih:** 28 Mart 2026  
**Hedef:** Eğitimde materyal bariyerini aşarak, disleksi tanılı çocuklar için kişiselleştirilmiş, dinamik ve "dost" bir öğrenme deneyimi sunmak.

---

## 1. Problem Tanımı ve Vizyon
**Eğitimde Materyal Bariyeri:** Mevcut ders kitapları; küçük fontlar, sıkışık satır aralıkları ve soyut dil kullanımı nedeniyle dislektik çocuklar için aşılması zor bir duvar oluşturuyor. 

**Çözüm:** LexiaBuddy, bu statik ve engelleyici materyalleri, dislektik beynin çalışma prensiplerine uygun (bütünsel, görsel ve sade) bir yapıya dönüştüren bir **"Bilişsel Tercüman"**dır.

---

## 2. Kullanıcı Analizi
* **Birincil Kullanıcı (Öğretmenler):** Sınıfındaki dislektik öğrencisi için genel müfredatı saniyeler içinde kişiselleştirilmiş bir materyale dönüştürmek isteyen eğitimciler.
* **İkincil Kullanıcı (Dislektik Çocuklar):** Ders çalışırken veya ödev yaparken metni kendi görsel/işitsel ihtiyaçlarına göre (font, renk, ses) özelleştiren 7-14 yaş arası öğrenciler.
* **Destekleyici Kullanıcı (Ebeveynler):** Evde çocuklarının okuma sürecini kolaylaştırmak ve akademik streslerini azaltmak isteyen aileler.

---

## 3. Yapay Zeka Rolü ve İşlem Hattı (AI Pipeline)

### 3.1. Görsel Ayıklama & OCR (Computer Vision)
* **İşlev:** Sayfa üzerindeki dikkat dağıtıcı unsurları (reklam, karmaşık grafik) temizleyip sadece öz bilgiyi dijital metne çevirir.
* **Teknoloji:** Google Cloud Vision API / Azure Form Recognizer.

### 3.2. Semantik Basitleştirme (NLP)
* **Hafif Seviye:** Metni bölümlere ayırır, zor kelimelerin yanına parantez içinde somut anlamlarını ekler.
* **İleri Seviye:** Karmaşık ve soyut cümleleri, anlamı bozmadan "Özne + Nesne + Yüklem" yapısındaki kısa cümlelere dönüştürür.
* **Teknoloji:** GPT-4o (Custom Prompt Engineering).

### 3.3. Multimodal Dönüşüm
* **Hecelendirme:** Türkçe dil kurallarına uygun, her hecenin farklı bir renkle (mavi/kırmızı) vurgulandığı yapı.
* **Zihin Haritası:** Metinden otomatik anahtar kelime çıkarımı ve görsel ağ haritası (Mind Map) üretimi.
* **Görsel Destek:** Soyut kavramları açıklayan piktogramlar ve ikonlar.

---

## 4. Uygulama Ekranları ve Akış

| Ekran | İşlev | Temel Özellikler |
| :--- | :--- | :--- |
| **1. Giriş & Profil** | Kullanıcıyı Tanıma | E-posta girişi, öğrenci seviye anketi, kişisel tercihler. |
| **2. Yükleme (Tarama)** | Veri Girişi | Kamera erişimi, PDF/JPEG sürükle-bırak yükleme alanı. |
| **3. Kontrol Paneli** | Özelleştirme | "Heceleri