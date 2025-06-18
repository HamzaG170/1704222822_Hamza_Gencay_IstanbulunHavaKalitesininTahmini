# İstanbul’un Hava Kalitesinin Tahmini  
### LSTM, GRU ve Transformer Tabanlı Derin Öğrenme Yöntemlerinin Karşılaştırmalı Analizi

Bu proje, İstanbul’un Başakşehir ilçesine ait günlük hava kalitesi ve meteorolojik veriler kullanılarak PM10 konsantrasyonunun tahmin edilmesini amaçlamaktadır. LSTM, GRU ve Transformer mimarileri karşılaştırılmış ve 2024–2026 yıllarını kapsayan ileriye dönük tahminler üretilmiştir.

---

##  Kullanılan Modeller

- **LSTM (Long Short-Term Memory)**
- **GRU (Gated Recurrent Unit)**
- **Transformer (Attention Tabanlı)**

Her model aynı veri setiyle eğitilmiş ve aşağıdaki metriklerle değerlendirilmiştir:

- **MAE** – Ortalama Mutlak Hata  
- **RMSE** – Kök Ortalama Kare Hata  
- **R²** – Belirleme Katsayısı  
- **MAPE** – Ortalama Yüzde Hata  

| Model       | MAE  | RMSE | R²     | MAPE (%) |
|-------------|------|------|--------|-----------|
| LSTM        | 7.83 | 11.02| 0.5582 | 21.85     |
| GRU         | 6.66 | 8.82 | 0.7168 | 18.00     |
| Transformer | 6.28 | 8.05 | 0.7640 | 18.47     |

---

## Veri Seti

- **Kaynaklar:** T.C. Çevre, Şehircilik ve İklim Değişikliği Bakanlığı, Meteoroloji Genel Müdürlüğü  
- **Dönem:** Ocak 2019 – Mart 2024  
- **Bölge:** İstanbul, Başakşehir ölçüm istasyonu  
- **Öznitelikler:**
  - **Kirleticiler:** PM10, SO₂, CO, NO₂, NOₓ, NO, O₃  
  - **Meteorolojik:** Sıcaklık, Nem, Rüzgar Hızı  

> Eksik veriler KNN (k=3) algoritmasıyla tamamlanmış ve tüm veriler MinMaxScaler ile normalize edilmiştir.

---

##  Modelleme Süreci

1.  Veri Temizleme ve Ön İşleme  
2.  Model Eğitimi (2019–2023 verisi)  
3.  Model Testi (2024 verisi)  
4.  730 Günlük Gelecek Tahmini (2024–2026)  
5.  Performans Karşılaştırması ve Görselleştirme  

---

## Katkı Sağlayanlar

- **Hamza Gençay** — 170422822  
- **Erdem Saçan** — 170422826  
- **Çağan Derbent** — 170421028  

---

## Üniversite Bilgisi

> Marmara Üniversitesi  
> Teknoloji Fakültesi  
> Bilgisayar Mühendisliği Bölümü  
> Bitirme Projesi – 2025  
> Danışman: Doç. Dr. Buket Doğan
