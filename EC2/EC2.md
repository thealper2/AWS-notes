EC2, sanal sunucu oluşturmaya yarayan servistir.

### Ücretlendirme Modelleri
- **On-Demand:** Saatlik sabit fiyat. Kısa süreli işler için ideal.
- **Reserved Instance:** 1 veya 3 yıllık reserve.
- **Scheduled Reserved Instance:** Reserved Instance ile aynıdır. Fakat bunda 24 saatlik değil, saatlik rezerve yöntemi kullanılır.
- **Covertible Reserved Instance:** Seçilen özellikteki makine yeterli gelmez ise makine geliştirilebilir.
- **Spot Instance:** Açık arttırma gibi. Makine verilen teklifteki fiyata düşerse kullanılır.
- **Dedicated Host:** Kiralik server rack.
- **Saving Plans:** Saatlik satın alım. Kontör gibi.

 
 - AMI: Amazon Machine İmage
 - AutoScaling: Load Balancing için makine ayarlaması
### EC2 Instance Çeşitleri
- **General Purpose (T-M-A):** Dengeli bilgi işlem, bellek ve ağ iletişimi. Web sunucuları, mikro servisler, geliştirme ortamları.
- **Compute Optimized (C):** Yüksek vCPU/ bellek oranı. Bilimsel modelleme, toplu işlem, reklam sunumu, yüksek ölçeklendirilebilir çok oyunculu oyun sunucusu
- **Memory Optimized (R-X-Z-U):** Büyük bellek içi işlemler için tasarlanmıştır. Yüksek performanslı veri tabanları, gerçek zamanlı büyük veri analitiği vb.
- **Storage Optimized (D-I-H):** Yüksek okuma yazma işlemleri; MapReduce, HDFS, Apache Kafka vb.
- **Accelerated Computing (F-P-G):** GPU'lar gibi donanım hızlandırıcıları kullanır. Makine / Derin öğrenme, akışkanlar dinamiği, hesaplamalı finans, sismik analiz, konuşma tanıma, özerk araçlar, ilaç keşfi.

**Instance Store**
- Instance'e fiziksel olarak bağlı.
- Kalıcı olmayan veri deposu
- Veri başka bir yere kopyalı değil
- Snapshot desteği yok

**Elastic Block Storage (EBS)
- Kalıcı veri deposu, Instance'den bağımsız.
- %99.999 erişilebilirlik garantisi
- AZ içinde birden fazla cihaza aynı veriler kopyalanıyor.
- Snapshot desteği

### Configurasyon
- Number of instances: Toplam makine sayısı
- Purchasing option: Spot isteği ayarı burada yapılır. Fiyat teklifi verme.
- IAM Role: Rol seçimi
- Shutdown behaviour: İşletim sisteminden kapatma komutu gelirse ne olacağını seçer. Stop, makine kapatılır fakat tekrar başlatılabilir. Terminate, makine kapatılır ve kaynaklar silinir.
- User data: Makine başlatılınca çalıştırılması istenen komutlar. Örneğin;

```shell
#!/bin/bash
yum update -y
```

### SSH Bağlantısı

```shell
chmod 400 cert.pem
ssh -i cert.pem ec2-user@<IP_ADDR>
```

### Elastic Load Balancer(ELB)
- Application Load Balancer (2016)
- Classic Load Balancer (2009)
- Network Load Balancer (2016)

### Placement Group
- Düzenlemek için tüm makineleri durdurmak gerekir
- Makineler arası bağlantıda düşük gecikme / yüksek aktarım gerektiğinde kullanılır.
- Aynı EC2 Instance tiplerinde kullanılır.
- Tek bir başlatma isteğiyle çalıştırıldığından sonradan makine eklenmez.


 