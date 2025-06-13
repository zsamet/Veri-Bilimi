# 🎯 Sadık Müşteri Tahmini – Online Retail ML Projesi

Bu proje, çevrim içi perakende sektöründe faaliyet gösteren bir işletmenin geçmiş satış verilerini kullanarak **müşterilerin yeniden alışveriş yapma olasılığını tahmin etmeyi** amaçlamaktadır. Proje kapsamında sınıflandırma algoritmaları uygulanmış, veri dengesizlikleri giderilmiş ve elde edilen sonuçlar görsellerle desteklenmiştir.

## 📊 Proje Amacı
- Sadık müşterilerin geçmiş alışveriş alışkanlıklarına göre tespit edilmesi
- Hedefli pazarlama kampanyalarına destek sağlanması
- Müşteri ilişkileri yönetiminde karar destek sistemi geliştirilmesi

## 🧠 Kullanılan Teknikler ve Kütüphaneler
- **Veri Madenciliği Yöntemi:** Sınıflandırma (Classification)
- **Algoritmalar:** Decision Tree, Random Forest
- **Dengesizlik Giderme:** SMOTE (Synthetic Minority Over-sampling)
- **Kütüphaneler:**  
  `pandas`, `numpy`, `scikit-learn`, `imbalanced-learn`, `matplotlib`, `seaborn`

## 🧾 Veri Seti
- Kaynak: [Kaggle - Online Retail Transactions Dataset](https://www.kaggle.com/datasets/abhishekrp1517/online-retail-transactions-dataset)
- Satır Sayısı: ~541.000  
- Alanlar: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

## ⚙️ Özellik Mühendisliği
- Müşteri bazlı toplam harcama, işlem sayısı, ortalama sepet büyüklüğü ve son alışverişten bu yana geçen süre gibi değişkenler çıkarıldı.
- `cutoff_date` sonrası alışveriş yapma durumu hedef değişken olarak etiketlendi (`Reordered`).

## 📈 Model Performansı
- SMOTE uygulanmadan önce azınlık sınıfta (yeniden alışveriş yapanlar) düşük F1-score gözlemlendi.
- SMOTE sonrası Random Forest modeliyle:
  - **Doğruluk (Accuracy):** ~%85
  - **Precision ve Recall:** Dengeli
  - **Confusion Matrix** ve **Feature Importance** görselleri ile desteklendi

## 🏢 İşletmeye Katkısı
- Sadık müşteriler önceden belirlenerek onlara özel teklifler sunulabilir.
- Pazarlama giderleri azaltılabilir, müşteri kaybı önlenebilir.
- Müşteri segmentasyon
