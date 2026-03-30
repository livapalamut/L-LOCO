# 📄 PRD: Liloco MVP (Minimum Viable Product)

**Sürüm:** 1.0  
**Durum:** Taslak / Geliştirme Aşamasında  
**Proje Sahibi:** Zeynep Liva Palamut  

---

## 1. Vizyon ve Kapsam
**Liloco**, market fişlerini analiz ederek sürdürülebilirliği "zahmetsiz ve ekonomik" hale getiren bir karar destek sistemidir. Bu PRD, uygulamanın temel işlevlerini (fiş okuma, veri eşleştirme ve akıllı öneri) içeren ilk web prototipini tanımlar.

---

## 2. Kullanıcı Hikayeleri (User Stories)
* **US1:** Bir kullanıcı olarak, market fişimin fotoğrafını yükleyebilmeliyim (Veri Girişi).
* **US2:** Bir kullanıcı olarak, aldığım ürünlerin karbon ayak izini grafiksel olarak görebilmeliyim (Farkındalık).
* **US3:** Bir kullanıcı olarak, yüksek emisyonlu ürünler yerine daha ucuz ve çevreci alternatifler alabilmeliyim (Optimizasyon).

---

## 3. Fonksiyonel Gereksinimler

### 3.1. Fiş İşleme Modülü (OCR & NLP)
* **Girdi:** Kullanıcı tarafından yüklenen `.jpg`, `.png` formatındaki görseller.
* **İşlem:** Görüntü işleme (OCR) ile metinlerin çıkarılması ve NLP ile ürün isimlerinin (örn: "Yar.Yağ.Süt") standardize edilmesi.
* **Çıktı:** Ürün adı, miktar ve fiyat bilgisini içeren yapılandırılmış veri (JSON).

### 3.2. Karbon ve Veri Analitik Motoru
* **Eşleştirme:** Çıkarılan ürünlerin yerel karbon katsayısı veri tabanıyla (LCA verileri) eşleştirilmesi.
* **Hesaplama:** Toplam sepet emisyonunun $E = \sum (Miktar \times Katsayı)$ formülüyle hesaplanması.

### 3.3. Akıllı Öneri Sistemi (Liloco AI)
* **Kriter:** "Karbon < Mevcut" VE "Fiyat <= Mevcut" VE "Besin Değeri >= Mevcut".
* **Aksiyon:** Bu kriterlere uyan en yakın yerel/mevsimsel ürünün kullanıcıya "Alternatif Öneri" olarak sunulması.

---

## 4. Teknik Stack (Teknoloji Yığını)

| Katman | Teknoloji | Neden? |
| :--- | :--- | :--- |
| **Frontend** | Streamlit / React | Hızlı prototipleme ve mühendislik dashboardları için ideal. |
| **Backend** | Python (FastAPI) | AI ve veri işleme kütüphaneleriyle (Pandas, NumPy) tam uyum. |
| **OCR Service** | Google Vision / Tesseract | Karmaşık fiş metinlerini yüksek doğrulukla okuma yeteneği. |
| **Database** | PostgreSQL / Supabase | Ürünlerin karbon katsayılarını ve kullanıcı geçmişini saklamak için. |

---

## 5. Kullanıcı Akışı (User Flow)
1. **Dashboard:** Kullanıcıyı karbon tasarrufu özetiyle karşılar.
2. **Upload:** Kullanıcı fişini sürükleyip bırakır.
3. **Processing:** AI, fişi satır satır analiz eder.
4. **Insights:** Karbon karnesi, bütçe analizi ve "Liloco Önerileri" ekranda belirir.
5. **Reward:** Tasarruf edilen karbon miktarına göre "Green-Coin" kazanılır.

---

## 6. Başarı Metrikleri (KPIs)
* **Hata Payı:** Ürün tanıma doğruluğu %85'in üzerinde olmalı.
* **Hız:** Görsel yüklemeden analize kadar geçen süre < 10 saniye olmalı.
* **Dönüşüm:** Kullanıcıya sunulan alternatiflerin tıklanma/beğenilme oranı %40+ olmalı.

---
*Bu doküman Liloco projesinin geliştirme sürecinde temel referans kaynağıdır.*
