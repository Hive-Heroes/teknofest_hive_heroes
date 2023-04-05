# teknofest_hive_heroes
#Acikhack2023


# NLP-Türkçe-Text-Sınıflandırma

### Takım Üyeleri
Berfin Duman

Bike Sönmez


TeknoFest 2023 Türkçe Doğal Dil İşleme Yarışması için oluşturduğumuz bu proje aşağılayıcı söylem içeren verilerin tespiti, sınıflandırılması ve elde edilen çıktıların endüstride bir use case olarak kullanılması fikrinden oluşuyor. 


Yarışma için geliştirdiğimiz projede amacımız, doğal dil işlemeyi kullanarak cümlelerdeki aşağılayıcı dili tespit etmek ve sınıflandırmak için Türkçe tabanlı doğal dil işleme teknikleri geliştirmeye odaklanmaktı. Projemiz, cinsiyetçi, ırkçı, saygısız veya aşağılayıcı konuşmaların varlığını doğru bir şekilde belirlemek için dil kalıplarını ve bağlamsal ipuçlarını tanımlamayı ve analiz etmeyi içerir. Ortaya çıkan teknik yeterliliğin sosyal medya platformları, çevrimiçi reklamcılık ve müşteri hizmetleri gibi çeşitli sektörlerde önemli etkileri olabileceğinden bu konuya da odaklandık.


Sınıflandırma problemini aşağıdaki adımlarla gerçekleştirdik:
* Gerekli kütüphane ve modülleri yükleme
* Veri setini yükleme ve Keşifsel Veri Analizi
* Metin ön işleme
* Metinden vektör çıkarma (Vektörleştirme)
* ML/DL amodelleri ve uygulamaları
* Çözüm

### 2.Adım: Veri seti yükleme ve EDA işlemleri

Proje için kullandığımız veri seti, aşağılayıcı söylemleri doğal dil işleme yöntemleri ile tespit etmek için kullandığımız **teknofest_train_final.csv** veri setidir.

Veri setinde belirlenecek durum, bir metinde aşağılayıcı söylem olup olmadığı durumudur. Yani 0 veya 1 olarak tahmin edilmelidir. Ayrıca aşağılayıcı söylem tahmin ediliyorsa bu söylem dökümünün verilen alt yapısı da (CİNSİYETÇİ, IRKÇI, KÜFÜR, KÜÇÜK) belirlenmelidir.

### 3.Adım: Preprocessing İşlemleri

Text processingte önemli yere sahip olan özel karakterleri silme, tokenizasyon, verilen metinlerden Türkçe stopwordsleri çıkarma, lemmatizasyon işelmleri gibi farklı işelmeleri ilgili kütüphaneler yardımıyla gerçekleştirdik.

### 4.Adım: Vektörizasyon

Bu adımda TF-IDF gibi yöntemler ile metinleri vektörize ederek modeller için uygun hale getirdik.

### 5.Adım: Modeller ve iyileştirmeler

Veri setine önce geleneksel sınıflandırma modellerini (Bernoulli Naive Bayes Classifier, Support Vector Machine, Logistic Regression, XGBClassifier, vb.)
daha sonrasında ise BERT, LSTM - BİLSTM gibi gelişmiş dil modellerinin bir kombinasyonundan oluşan ensemble bir model uygulayarak modellerin başarısını test ettik ve karşılaştırmalar yaptık. Bu karşılaştırmalar sonucunda birkaç farklı modelin bir arada kullanılabildiği ensemble bir yaklaşım sergiledik. Modellerin başarılarını etkileyen faktörleri inceleyerek modellerde iyileştirmeler yapmaya çalıştık. 



### 6. Adım: Sonuç

Son olarak çıktılarımız doğrultusunda, yaptığımız projenin  Telco ve OTT sektöründe olası kulanım alanlarını araştırarak ve yeni fikirler üreterek bunları bir use case modeline aktardık.

Macro-F1 : 0.95 


## Gerekli kütüphaneler: 
> gradio              3.24.1

> pandas              1.5.2

> nltk                3.7

> session_info        1.0.0

> sklearn             1.2.2

> torch               1.13.1+cpu

>transformers        4.26.1




















