# CASE STUDY
## 1.Görev
Linkte verilen uygulama kodlarını github reposuna yüklemek için sırasıyla
```
git clone <depo url>
git add .
git commit -m ""
git push orgin master
````
komutlarını kullandım.
## 2.Görev
Uygulamanın docker üzerinde çalışması için bir dockerfile oluşturmam gerekiyordu. Bunun için :
```
FROM python:3.11
COPY ./app
WORDIR /app
RUN pip install -r requşrements.txt
EXPOSE 5000
CMD python app.py
```
şeklinde bir dockerfile oluşturdum.
FROM komutu ile temel imaj belirtilir. Temel imaj, imajın inşa edileceği imajdır.
COPY imaj için gerekli dosyaları kopyalar.
WORKDIR komutu çalışma dizinini ayarlar. Dockerdile'da çalıştırılan komutlar için varsayılan çalışma dizinidir.
RUN imaj için gerekli komutları çalıştırır. Bu komutlar imajın kurulumu ve yapılandırmasını gerçekleştirir.
EXPOSE imaj için gerekli bağlanto noktalarını açar. Bu bağlantı noktaları imajın konteynerleri tarafından kullanılır.
CMD imajın başlangıç komutunu belirtir. Başlangıç komutu imajın konteynerinin başlatılması için çalıştırılan komuttur.
## 3.Görev
Docker Hub üzerinden abpolat/ahmetbarispolat adında bir image reposu oluşturdum. Daha sonra ;
```
docker build -t studycase .
```
adından bir image oluşturdum ve docker huba yükledim. -t seçeneği, docker imaja bir etiket atamak için kullanılır.
## 4.Görev
Son olarak oluşturduğum imajı container olarak çalıştırmak için;
```
docker run -d -p 5001:5000 studycase2
```
kodunu kullandım. -d(detach) docker containerın arka planda çalıştırır ve kullanıcının terminaliyle bağlantısını serbest kılar. -p(port) yerel makinedeki portu docker containerde çalışan bir uygulama portuna bağlanmasını sağlar.


