# 🌱 Carbon Footprint Analysis of Inditex Group Products

Bu proje, tekstil sektöründe faaliyet gösteren şirketlerin (özellikle Inditex grubu örnek alınarak) ürün bazlı karbon ayak izlerini analiz etmeyi amaçlar. Python ile geliştirilmiş bu analiz, ürün tipi, marka, üretim süreçleri ve çevresel etkiler gibi unsurları dikkate alarak çevresel etkilerin daha iyi anlaşılmasını sağlar.

---

## 📁 Proje Yapısı

- `carbon_footprint_analysis.ipynb` – Ana Jupyter Notebook dosyası. Veriyi işler, analiz eder ve görselleştirir.
- `inditex_120_product_synthetic_dataset.csv` – Sentetik ürün verilerini içeren CSV dosyası.

---

## 📊 Kullanılan Kütüphaneler

- `pandas` – Veri yükleme ve düzenleme
- `numpy` – Sayısal işlemler
- `matplotlib` & `seaborn` – Görselleştirme


## 🔍 Yapılan Analizler

- 📦 Veri Yükleme ve İnceleme
  - Dataset boyutu, sütun tipi inceleme, eksik değer kontrolü
- 📊 Ürün Tipi ve Marka Dağılımları
  - Şirket bazlı ürün sayısı
  - Ürün tiplerinin frekans dağılımı
- 🌱 Çevresel Etki Analizleri
  - Karbon salınımı (CO₂e), enerji ve su tüketimi
  - Ürünlerin ortalama karbon salımı ve dağılımları
  - Görselleştirmelerle desteklenen sezgisel analizler

---

## 📷 Örnek Görselleştirmeler

- Barplot: Markalara göre ürün sayısı
- Countplot: Ürün tiplerine göre dağılım
- Scatterplot/Boxplot: Karbon salımı - enerji ilişkisi

---

## 🚀 Nasıl Kullanılır?

1. Gerekli kütüphaneleri kurun:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

2. Proje klasörüne veri dosyasını (`inditex_120_product_synthetic_dataset.csv`) yerleştirin.

3. `carbon_footprint_analysis.ipynb` dosyasını Jupyter Notebook'ta açarak adım adım çalıştırın.

---

## 📌 Ekstra: Eksik Veri Kontrolü

```python
print("Eksik veri kontrolü:")
print(df.isnull().sum())

# Eksik veriler varsa doldurma örneği
if df.isnull().sum().any():
    print("Eksik veriler tespit edildi, dolduruluyor...")
    df.fillna(df.mean(numeric_only=True), inplace=True)
else:
    print("Eksik veri bulunamadı.")
```

---

## 🎯 Amaç

Bu çalışma, sürdürülebilirlik ve çevresel etki farkındalığını artırmak isteyen veri bilimi uygulamaları için örnek bir temel sunar. Şirketlerin karbon salımlarını görsel ve analitik olarak takip etmesini sağlayarak daha bilinçli üretim stratejileri geliştirmelerine yardımcı olmayı amaçlar.

## 📌 Not

Bu analizde kullanılan veriler sentetik olarak oluşturulmuştur ve gerçek Inditex ürünlerine ait verileri temsil etmez. Çalışma yalnızca akademik ve öğrenim amaçlıdır.