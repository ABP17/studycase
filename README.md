# CASE STUDY
## 1.Görev
Linkte verilen uygulama kodkarını github reposuna yüklemek için sırasıyla
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
## 3.Görev
Docker Hub üzerinden abpolat/ahmetbarispolat adında bir image reposu oluşturdum. Daha sonra ;
```
docker build -t studycase .
```
adından bir image oluşturdum ve docker huba yükledim.
## 4.Görev
Son olarak oluşturduğum imajı container olarak çalıştırmak için;
```
docker run -d -p 5001:5000 studycase2
```
kodunu kullandım.


