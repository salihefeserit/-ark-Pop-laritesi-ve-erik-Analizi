## Giriş
---
Bu Repo'da Spotify şarkı verilerini içeren bir veri seti kullandım
##### Data Cleaning
- Bu veri seti üzerinde sayısal değere dönüştürülemeyen **track_name** özellikleri gibi NaN değerler içeren satırlar veri setinden temizlendi.
- Aynı şekilde eğitilecek modelleri olumsuz etkileyebilecek tekrarlayan veriler temizlendi.
- Gereksiz özellikler verisetinden silindi.
##### Korelasyon Matrisi
- Sayısal değerler içeren özelliklerin birbirleri ile ilişkisini gösteren bir Korelasyon matrisi oluşturuldu ve bu görselleştirildi.
##### Görselleştirme
- Veri setindeki en popüler bazı özelliklere sahip olan satırlar görselleştirildi
- Özelliklerin birbirleri ile ilişkisini gösteren görseller oluşturuldu.
##### Data Preprocessing
- Veri setine hali hazırda bulunan bazı özellikleri dönüştürerek veya kombine edilerek yeni özellikler eklendi.
- Eklenen özellikler sonucunda gereksiz hale gelen özellikler veri setinden temizlendi.
- Değer aralığı fazla olan özelliklerin değerleri ölçeklendirildi.
- Makinenin anlayamayağı türden özellikleri sayısal özelliklere dönüştürdüm.
##### Feature Engineering
###### Regresyon Problemi
- Sürekli değerler içeren **popularity** etiketi için farklı regresyon modelleri ile tahminler yapıldı.
- Bu modellerin hataları **MSE** ve **RMSE** yoluyla karşılaştırıldı.
- Bu modeller üzerinde **Çapraz Doğrulama (Cross Validation)** yapıldı ve birbirleri ile karşılaştırıldı.
- En düşük hata (RMSE)'ye sahip olan **Random Forest Regressor** üzerinde **Hiperparametre Optimizasyonu** yapmaya çalışıldı.
- Bu optimizasyon sonucunda küçük de olsa hatadan kazanç elde edildi.
###### Classification Problemi
- Sürekli değerler içermeyen **explicit** etiketi için farklı sınıflandırma modelleri ile tahminler yapıldı.
- Bu modeller için **Accuracy**, **Precision**, **Recall** ve **f1-score** gibi metrikleri gösteren **Sınıflandırma Raporları** oluşturuldu ve görselleştirildi.
- Aynı modellerde tahminleri kullanarak **Karışıklık Matris**'leri oluşturuldu.
- Modeller üzerinde çapraz doğrulama yapıldı ve sonucunda çıkan doğruluk ve istikrar (std)'yi değerlendirildi.
- En istikrarlı ve en yüksek doğruluğa sahip LinearSVC modeli üzerinde Hiperparametre Optimizasyonu yapmaya çalışıldı.
## Metrikler
---
- **Data Cleaning** ve **Feature Engineering** sayesinde modellerin doğruluğu ve güvenilirliği artırıldı.
- **Regresyon problemlerinde** Random Forest Regressor, (RMSE'den dolayı)
- **Sınıflandırma problemlerinde** ise LinearSVC (Cross Validation) öne çıktı.
- Çapraz doğrulama ile modelin performansını ve istikrarını değerlendirmeyi öğrendim.
- Hiperparametre optimizasyonu ile modellerin performansı daha da iyileştirilmeye çalışıldı.
- Hiperparametre optimizasyonu için parametreleri içeren sözlük daha büyük olsaydı belkide daha optimal sonuca ulaşılabilirdi.

## Sonuç ve Gelecek Çalışmalar
---
- Sonuçlar, müzik verisi üzerinde makine öğrenmesi uygulamalarının etkili şekilde kullanılabileceğini gösteriyor.

- Bootcamp sonrasında zaman buldukça bu projeyi daha optimize hale getirmeye çalışacağım. Verileri yeterince verimli işleyemediğimi düşünüyorum.
- Ek olarak aynı proje üzerinde farklı özellikler ile de çalışmayı planlıyorum.
- Ondan sonra Gözetimsiz Öğrenme ile başka bir proje geliştirmeyi ve bunun sayesinde onun da inceliklerini kavramayı planlıyorum. Ayrıca GPU kütüphanelerine göz atacağım.
## Linkler
---
[Kaggle Notebook](https://www.kaggle.com/code/salihefeerit/analyzing-popularity-and-content-sensitivity)

[Veriseti](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)

