# Akbank Derin Öğrenme Bootcamp Projesi: Görüntü Sınıflandırma

[cite_start]Bu proje, Akbank Derin Öğrenme Bootcamp'i kapsamında geliştirilmiştir[cite: 1]. [cite_start]Projede, bir görüntü veri seti kullanılarak CNN (Convolutional Neural Network) tabanlı bir derin öğrenme modeli oluşturulmuş ve eğitilmiştir[cite: 2].

## 1. Projenin Amacı

Bu projenin temel amacı, [Buraya kendi projenizin amacını yazın. [cite_start]Örneğin: "Intel Image Classification veri setini kullanarak doğal sahne görüntülerini (orman, dağ, deniz vb.) 6 farklı sınıfa ayırabilen bir model geliştirmektir."][cite: 9]. [cite_start]Bu sayede görüntü sınıflandırması, veri analizi ve model değerlendirme konularında pratik deneyim kazanılması hedeflenmektedir[cite: 3].

## 2. Veri Seti Hakkında Bilgi

* [cite_start]**Veri Seti Adı:** [Örn: Intel Image Classification] [cite: 71, 75]
* [cite_start]**Veri Seti Türü:** [Örn: Çok Sınıflı Görüntü Sınıflandırma (Multiclass Image Classification)] [cite: 72]
* [cite_start]**Sınıf Sayısı:** [Örn: 6] [cite: 72]
* [cite_start]**Sınıflar:** [Örn: Binalar, Orman, Buzul, Dağ, Deniz, Cadde] [cite: 73]
* [cite_start]**Toplam Görüntü Sayısı:** [Örn: ~25.000 eğitim, 14.000 test görüntüsü] [cite: 74]
* **Açıklama:** [Buraya veri setiyle ilgili kısa bir açıklama ekleyin. [cite_start]Örn: "Veri seti, farklı doğal ve yapay ortamların sınıflandırılması için oluşturulmuştur."] [cite: 75]

## 3. Kullanılan Yöntemler

[cite_start]Projenin geliştirilmesi sırasında aşağıdaki yöntemler ve teknolojiler kullanılmıştır[cite: 11]:

* **Veri Ön İşleme:**
    * Görüntülerin yeniden boyutlandırılması ve normalize edilmesi.
    * [cite_start]Veri setinin eğitim (train), doğrulama (validation) ve test setlerine ayrılması[cite: 19].
    * [cite_start]**Data Augmentation (Veri Çoğaltma):** Overfitting'i önlemek ve model başarımını artırmak için `Rotation`, `Flip`, `Zoom` gibi teknikler kullanılmıştır[cite: 21, 23, 24, 25].
* **Model Mimarisi:**
    * [cite_start]CNN tabanlı bir model oluşturulmuştur[cite: 29].
    * [cite_start]Modelde `Convolutional` [cite: 30][cite_start], `Pooling` [cite: 31][cite_start], `Dropout` [cite: 32] [cite_start]ve `Dense` [cite: 33] katmanları kullanılmıştır.
    * [cite_start]Aktivasyon fonksiyonu olarak `ReLU` ve `Softmax` tercih edilmiştir[cite: 34].
* **Model Değerlendirme:**
    * [cite_start]Epoch bazında `Accuracy` ve `Loss` grafikleri ile modelin öğrenme süreci izlenmiştir[cite: 37].
    * [cite_start]`Confusion Matrix` ve `Classification Report` ile modelin sınıf bazındaki performansı ölçülmüştür[cite: 38].
    * [cite_start]`Grad-CAM` tekniği ile modelin test görüntüleri üzerinde hangi bölgelere odaklandığı görselleştirilmiştir[cite: 39, 40].
* **Hiperparametre Optimizasyonu:**
    * [cite_start]En iyi model başarımını elde etmek için `learning rate` [cite: 48][cite_start], `batch size` [cite: 49] [cite_start]ve `dropout oranı` [cite: 46] gibi parametreler üzerinde denemeler yapılmıştır.

## 4. Elde Edilen Sonuçlar

[Bu bölüme projenizin sonuçlarını özet halinde yazın. [cite_start]Örneğin:] [cite: 12]

* Geliştirilen model, test veri seti üzerinde **%XX**'lik bir doğruluk (accuracy) skoruna ulaşmıştır.
* Loss ve accuracy grafikleri, modelin başarılı bir şekilde öğrendiğini ve ciddi bir overfit problemi yaşamadığını göstermektedir.
* Confusion matrix sonuçlarına göre model, özellikle 'orman' ve 'deniz' sınıflarını yüksek başarıyla tahmin ederken, 'bina' ve 'cadde' gibi birbirine benzer sınıflarda zorlanmıştır.
* Grad-CAM görselleştirmeleri, modelin doğru sınıflandırma yaparken nesnelerin belirgin özelliklerine odaklandığını doğrulamıştır.

## 5. Kaggle Notebook Linki

Projenin tüm teknik detaylarını, kodlarını ve çıktılarını içeren Kaggle notebook'una aşağıdaki linkten ulaşabilirsiniz:

[cite_start][Buraya Kaggle Notebook'unuzun Paylaşım Linkini Yapıştırın] [cite: 13]
