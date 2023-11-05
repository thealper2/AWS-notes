EFS, basit, ölçeklenebilir ve elastik dosya depolama alanı sağlar. Kullanımı kolay bir arayüzü vardır. EFS, uygulamaların işleyişini bozmadan, dosya ekleme-kaldırma talepleri üzerine, esnek bir şekilde ölçeklendirilebilmek için üretilmiştir. Bu sayede, uygulamalr ihtiyaç duydukları anda ihtiyaç duydukları depolama alanına sahip olur.

- Ölçeklenebilirdir.
- Bir disk değildir Üzerinde işletim sistemi kurulmaz.
- Aylık GB depolama alanı ödenir.
- NFS tabanlıdır.
- Dosya eklendikçe otomatik büyür ve dosya silindikçe otomatik küçülür (esnek).
- Aynı anda birden fazla makine tarafından erişilebilir.

```shell
# Makine 1
sudo yum install -y amazon-efs-utils
sudo mkdir efs1
sudo mount -t efs -o tls <id>:/ efs1
sudo echo "EFS1" >> file.txt

# Makine 2
sudo yum install -y amazon-efs-utils
sudo mkdir efs2
sudo mount -t efs -o tls <id>:/ efs2
sudo echo "EFS2" >> file.txt
```