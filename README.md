Akbank Derin Öğrenme Bootcamp Projesi: Trafik İşareti Tanıma Sistemi
Bu proje, Akbank Derin Öğrenme Bootcamp'i kapsamında geliştirilmiştir. Projede, "Traffic Sign Detection" veri seti kullanılarak trafik işaretlerini 43 farklı sınıfta tanıyabilen bir CNN (Evrişimli Sinir Ağı) modeli tasarlanmış, eğitilmiş ve optimize edilmiştir.

1. Projenin Amacı
Bu projenin temel amacı, görüntüdeki trafik işaretlerini tespit edip doğru bir şekilde sınıflandırabilen bir derin öğrenme modeli geliştirmektir. Bu sayede, otonom sürüş sistemleri gibi teknolojilerin temelini oluşturan görüntü sınıflandırma, veri analizi ve model değerlendirme konularında pratik deneyim kazanılması hedeflenmektedir.


2. Veri Seti Hakkında Bilgi

Veri Seti Adı: Traffic Sign Detection 


Veri Seti Türü: Görüntü Sınıflandırma (43 sınıf) 


Sınıf Sayısı: 43 


Toplam Görüntü Sayısı: ~50.000 görüntü 


Açıklama: Veri seti, farklı trafik işaretlerini içeren görsellerden oluşmaktadır ve modelin bu işaretleri ayırt etmesi beklenmektedir.


Veri Seti Linki: https://www.kaggle.com/datasets/valentynsichkar/traffic-signs-preprocessed/data 

3. Kullanılan Yöntemler
Projenin geliştirilmesi sırasında aşağıdaki yöntemler ve teknolojiler kullanılmıştır:

Veri Ön İşleme:

Görüntülerin modele uygun formatlara dönüştürülmesi ve 0-1 aralığına normalize edilmesi.

Veri setinin eğitim (train), doğrulama (validation) ve test setlerine ayrılması.

Model Mimarisi:

CNN tabanlı bir model oluşturulmuştur.

Modelde 

Convolutional , 

Pooling , 

Dropout ve 

Dense  katmanları kullanılmıştır.

Aktivasyon fonksiyonu olarak 

ReLU ve Softmax tercih edilmiştir.

Model Değerlendirme:

Epoch bazında 

Accuracy ve Loss grafikleri ile modelin öğrenme süreci izlenmiştir.


Confusion Matrix ve Classification Report ile modelin sınıf bazındaki performansı detaylıca ölçülmüştür.


Grad-CAM tekniği ile modelin bir trafik işaretini tanırken görüntünün hangi bölgelerine odaklandığı görselleştirilmiştir.

Hiperparametre Optimizasyonu:

En iyi model başarımını elde etmek için Keras Tuner kütüphanesi kullanılmıştır.

Öğrenme oranı (learning rate) , katmanlardaki filtre/nöron sayısı ve dropout oranı  gibi parametreler üzerinde otomatik denemeler yapılmıştır.




4. Elde Edilen Sonuçlar
Keras Tuner ile optimize edilip 25 epoch boyunca eğitilen final modeli, test veri seti üzerinde %97.74'lük bir doğruluk (accuracy) skoruna ulaşmıştır.

Loss ve accuracy grafikleri, modelin başarılı bir şekilde öğrendiğini ve doğrulama (validation) eğrilerinin eğitim eğrilerini yakından takip etmesiyle overfitting'in kontrol altında tutulduğunu göstermektedir.

Confusion matrix sonuçlarına göre model, özellikle belirgin şekil ve renklere sahip olan "Dur", "Geçiş Hakkı Ver" veya çeşitli "Hız Limiti" gibi işaretleri çok yüksek başarıyla tanımaktadır.

Grad-CAM görselleştirmeleri, modelin doğru sınıflandırma yaparken tabelanın şekline ve üzerindeki sembole odaklandığını, arka plandaki gürültüyü ise büyük ölçüde göz ardı ettiğini doğrulamıştır.

5. Kaggle Notebook Linki
Projenin tüm teknik detaylarını, kodlarını ve çıktılarını içeren Kaggle notebook'una aşağıdaki linkten ulaşabilirsiniz:

https://www.kaggle.com/code/hamdiemirhanetin/notebookf3a449d8ba
