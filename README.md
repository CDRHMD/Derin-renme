# Akbank Derin Öğrenme Bootcamp Projesi: Trafik İşareti Tanıma Sistemi

Bu proje, Akbank Derin Öğrenme Bootcamp'i kapsamında geliştirilmiştir. Projede, "Traffic Sign Detection" veri seti kullanılarak trafik işaretlerini 43 farklı sınıfta tanıyabilen bir CNN (Convolutional Neural Network) modeli tasarlanmış ve eğitilmiştir.

## 1. Projenin Amacı

[cite_start]Bu projenin temel amacı, görüntüdeki trafik işaretlerini tespit edip doğru bir şekilde sınıflandırabilen bir derin öğrenme modeli geliştirmektir[cite: 90]. [cite_start]Bu sayede, otonom sürüş sistemleri gibi teknolojilerin temelini oluşturan görüntü sınıflandırma, veri analizi ve model değerlendirme konularında pratik deneyim kazanılması hedeflenmektedir[cite: 3].

## 2. Veri Seti Hakkında Bilgi

* [cite_start]**Veri Seti Adı:** Traffic Sign Detection [cite: 87]
* [cite_start]**Veri Seti Türü:** Nesne Tespiti (Object Detection) / Sınıflandırma (Classification) (43 sınıf) [cite: 88]
* [cite_start]**Sınıf Sayısı:** 43 [cite: 88]
* [cite_start]**Toplam Görüntü Sayısı:** ~50.000 görüntü [cite: 89]
* [cite_start]**Açıklama:** Veri seti, farklı trafik işaretlerini içeren görsellerden oluşmaktadır ve modelin bu işaretleri ayırt etmesi beklenmektedir[cite: 90].
* [cite_start]**Veri Seti Linki:** https://www.kaggle.com/datasets/valentynsichkar/traffic-signs-preprocessed/data [cite: 91]

## 3. Kullanılan Yöntemler

Projenin geliştirilmesi sırasında aşağıdaki yöntemler ve teknolojiler kullanılmıştır:

* **Veri Ön İşleme:**
    * [cite_start]Görüntülerin modele uygun formatlara dönüştürülmesi ve normalize edilmesi[cite: 19].
    * [cite_start]Veri setinin eğitim (train), doğrulama (validation) ve test setlerine ayrılması[cite: 19].
    * [cite_start]**Data Augmentation (Veri Çoğaltma):** Modelin farklı ışık ve açı koşullarına karşı daha dayanıklı olmasını sağlamak ve ezberlemeyi (overfitting) önlemek amacıyla `Rotation`, `Flip` ve `Zoom` gibi teknikler kullanılmıştır[cite: 21, 23, 24, 25].
* **Model Mimarisi:**
    * [cite_start]CNN tabanlı bir model oluşturulmuştur[cite: 29].
    * [cite_start]Modelde `Convolutional` [cite: 30][cite_start], `Pooling` [cite: 31][cite_start], `Dropout` [cite: 32] [cite_start]ve `Dense` [cite: 33] katmanları kullanılmıştır.
    * [cite_start]Aktivasyon fonksiyonu olarak `ReLU` ve `Softmax` tercih edilmiştir[cite: 34].
* **Model Değerlendirme:**
    * [cite_start]Epoch bazında `Accuracy` ve `Loss` grafikleri ile modelin öğrenme süreci izlenmiştir[cite: 37].
    * [cite_start]`Confusion Matrix` ve `Classification Report` ile modelin sınıf bazındaki performansı detaylıca ölçülmüştür[cite: 38].
    * [cite_start]`Grad-CAM` tekniği ile modelin bir trafik işaretini tanırken görüntünün hangi bölgelerine odaklandığı görselleştirilmiştir[cite: 39, 40].
* **Hiperparametre Optimizasyonu:**
    * [cite_start]En iyi model başarımını elde etmek için öğrenme oranı (learning rate) [cite: 48][cite_start], yığın boyutu (batch size) [cite: 49] [cite_start]ve dropout oranı [cite: 46] gibi parametreler üzerinde denemeler yapılmıştır.

## 4. Elde Edilen Sonuçlar

* Geliştirilen model, test veri seti üzerinde **[Buraya modelinizin test doğruluğunu yazın, örn: %98.5]**'lik bir doğruluk (accuracy) skoruna ulaşmıştır.
* Loss ve accuracy grafikleri, modelin başarılı bir şekilde öğrendiğini ve düzenlileştirme (regularization) teknikleri sayesinde overfitting'in kontrol altında tutulduğunu göstermektedir.
* Confusion matrix sonuçlarına göre model, özellikle belirgin şekil ve renklere sahip olan "Dur" veya "Hız Limiti" gibi işaretleri yüksek başarıyla tanırken, birbirine benzeyen "Sola Tehlikeli Viraj" ve "Sağa Tehlikeli Viraj" gibi işaretlerde daha düşük performans göstermiştir.
* Grad-CAM görselleştirmeleri, modelin doğru sınıflandırma yaparken tabelanın şekline ve üzerindeki sembole odaklandığını doğrulamıştır.

## 5. Kaggle Notebook Linki

Projenin tüm teknik detaylarını, kodlarını ve çıktılarını içeren Kaggle notebook'una aşağıdaki linkten ulaşabilirsiniz:

**[Buraya Kaggle Notebook'unuzun Paylaşım Linkini Yapıştırın]**
