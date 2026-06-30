# australia-rain-prediction-lstm

# 🌧️ Avustralya Yağmur Tahmini - LSTM Derin Öğrenme Projesi

Bu proje, Avustralya'nın farklı bölgelerine ait geçmiş hava durumu zaman serisi verilerini analiz ederek, gelecek günlerde yağmur yağıp yağmayacağını tahmin etmek amacıyla geliştirilmiş bir **Derin Öğrenme (Deep Learning)** projesidir.



## 🧠 Model Mimarisi ve Yaklaşım
Proje kapsamında, zaman serisi ve ardışık (sequential) veriler üzerinde yüksek performans gösteren **Yapay Sinir Ağları (Artificial Neural Networks)** mimarisi kullanılmıştır:
- **Veri Seti:** Avustralya'nın çoklu meteoroloji istasyonlarından toplanan sıcaklık, nem, rüzgar hızı ve yağış miktarı gibi parametreleri içerir.
- **Önişleme (Preprocessing):** Eksik verilerin (Missing Values) doldurulması, kategorik değişkenlerin sayısallaştırılması ve derin öğrenme modelinin kararlı çalışması için özellik ölçekleme (MinMax / Standard Scaling) işlemleri uygulanmıştır.
- **Model Katmanları:** Keras ve TensorFlow altyapısı kullanılarak `Sequential` mimaride, aşırı öğrenmeyi (overfitting) engellemek için `Dropout` katmanlarıyla desteklenmiş ve sınıflandırma için `Dense` katmanları içeren bir derin sinir ağı tasarlanmıştır.

## 📂 Proje Yapısı
- `main.py`: Veri önişleme, model kurulumu, eğitim süreci ve değerlendirme kodlarını içerir.
- `weatherAUS.csv`: Ana meteorolojik zaman serisi veri kümesi.
- `train (1).csv` & `test (1).csv`: Eğitim ve test süreçleri için ayrıştırılmış veri setleri.
- `sample_submission.csv`: Model tahmin sonuçlarının dışa aktarılma formatı.

## 📦 Kurulum ve Çalıştırma

1. Repoyu bilgisayarınıza klonlayın:
   ```bash
   git clone [https://github.com/kullanici-adiniz/australia-rain-prediction-lstm.git](https://github.com/kullanici-adiniz/australia-rain-prediction-lstm.git)
   cd australia-rain-prediction-lstm
