Amazon SageMaker, veri etiketleme, model oluşturma, eğitim, ayarlama ve dağıtım hizmetleri sağlayan, tam olarak yönetilen bir makine öğrenimi iş akışı platformudur. SageMaker, veri bilimcilerin ve geliştiricilerin ölçeklenebilir AI/ML modellerini kolay ve verimli bir şekilde oluşturmasına olanak sağlar.

**Training Job**
- Amazon S3 URL'si (eğitim verileri için): Eğitim verilerinin bulunduğu yer.
- Hesaplama kaynakları: Amazon SageMaker, Amazon SageMaker tarafından yönetilen örnekleri kullanarak modeli eğitecektir.
- Amazon S3 URL'si (çıktı): Eğitim çıktısının barındırılacağı yer.
- Amazon EC2 Registry Path: Eğitim kodunun depolandığı yer.
* Amazon SageMaker, eğitilen model yapıtlarını bir S3 kovasına kaydeder.

**Train Seçenekleri**
* **Amazon SageMaker tarafından sağlanan algoritmalar**: Lineer, XGBoost, KMeans gibi hazır eğitim algoritmaları sağlar.
* **Popüler derin öğrenme çerçevelerini kullanarak özel kod eğitimi:** Model eğitimi için TensorFlow veya Apache MXNet ile özel python kodu.
* **Kendi algoritmalarınız:** Kod bir docker konteynerine yerleştirilebilir ve ardından Amazon SageMaker CreateTrainingJob API çağrısına görüntünün kayıt yolu sağlanabilir.
* **AWS Marketplace:** Amazon pazarından bir algoritma seçin. YOLO vb.
* **Apache Spark:**  Apache Spark, Amazon SageMaker ile modelleri eğitmek için kullanılabilir.

**AWS SageMaker Studio**
* Jupyter Lab'in geliştirilmiş hali.
* AI/ML modellerini tek bir yerde oluşturabilecekleri, eğitebilecekleri ve dağıtabilecekleri web tabanlı görsel bir arayüzüdür.

**AWS SageMaker Canvas**
* Kod yazmadan bir makine öğrenimi modeli oluşturmasını, eğitmesini ve test etmesini sağlar.
- S3'ten veya başka bir kaynaktan veri içe aktarılabilir.
- Model performansını değerlendirebilir.
- Çıkarım ve tahminler oluşturabilir.
- Modeli SageMaker Studio'ya aktarabilir.
