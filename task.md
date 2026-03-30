# 🛠 Liloco: Geliştirme Yol Haritası & Görev Listesi (tasks.md)

Bu dosya, Liloco MVP sürümüne ulaşmak için tamamlanması gereken teknik adımları içerir.

## 🏗 Aşama 1: Hazırlık ve Ortam Kurulumu
- [ ] Python çalışma ortamının kurulması (Virtual Environment).
- [ ] Gerekli temel kütüphanelerin belirlenmesi (`Streamlit`, `Pandas`, `Pytesseract` veya `EasyOCR`).
- [ ] GitHub reposunun yerel bilgisayara klonlanması.

## 👁 Aşama 2: Fiş İşleme (OCR) Modülü
- [ ] Kullanıcının fotoğraf yükleyebileceği basit bir arayüz tasarlanması (Streamlit `file_uploader`).
- [ ] Yüklenen görseldeki metinleri okuyacak OCR entegrasyonunun yapılması.
- [ ] **Challenge:** Karmaşık fiş metinlerinden (örn: "DOM.SAL.1KG") sadece ürün adı ve fiyatı ayıklayan bir temizleme fonksiyonu yazılması.

## 📊 Aşama 3: Veri Seti ve Eşleştirme
- [ ] Temel ürünlerin karbon katsayılarını içeren bir `carbon_data.csv` oluşturulması.
- [ ] OCR'dan gelen ürün isimlerini, veri setindeki en yakın ürünle eşleştiren bir mantık (Fuzzy Matching) kurulması.
- [ ] Toplam karbon ayak izini hesaplayan fonksiyonun yazılması.

## 💡 Aşama 4: Liloco Öneri Motoru (AI Logic)
- [ ] Yüksek karbonlu ürünleri tespit eden filtrenin yazılması.
- [ ] "Daha düşük karbon + Daha uygun fiyat" kriterine göre alternatif ürün öneren algoritmanın kodlanması.
- [ ] Önerilerin kullanıcıya görsel bir kart yapısıyla sunulması.

## 🎨 Aşama 5: Kullanıcı Arayüzü (Frontend) İyileştirme
- [ ] Dashboard ekranının tasarlanması (Toplam Karbon Skoru, Harcama Özeti).
- [ ] Tasarruf edilen karbon miktarını "Dikilen Ağaç Sayısı" gibi somut verilere dönüştüren görsellerin eklenmesi.
- [ ] Liloco marka renklerinin (Yeşil & Beyaz) arayüze uygulanması.

## 🚀 Aşama 6: Yayına Alma ve Test
- [ ] Uygulamanın `Streamlit Cloud` veya `Hugging Face Spaces` üzerinde ücretsiz canlıya alınması.
- [ ] Farklı market fişleriyle (Migros, BİM, Şok) sistemin test edilmesi.
- [ ] Hataların (Bug) ayıklanması ve nihai dokümantasyonun güncellenmesi.

---
*Gelecek Planı: Market sadakat kartlarıyla (API entegrasyonu) otomatik veri çekme denemeleri.*
