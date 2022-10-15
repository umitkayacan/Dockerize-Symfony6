# Docker ile Symfony 6 Kurulumu

Symfony 6'nın kurulum gereksinimlerine göre docker image'ları seçilmiştir. `docker-compose.yml` içinde 

- PHP8

- MYSQL8

- NginX (8080 portunu kullanacağız)

image'ları kullanılmıştır.

# Kurulum
Repository'i bir dizine clonlayın ve docker-compose.yml dosyasının olduğu dizine cd komutu ile geçip
```bash
  docker-compose up -d 
```
komutu ile php8, mysql 8 ve Nginx kurulumu tamamlanır ve containerlar ayağı kalkar.



# Docker üzerinde çalışan containerları listeleme

```bash
  docker ps
```
komutu ile aşağıda gördüğümüz gibi containerlar listelenecektir. 

Şimdi de PHP container'ının içine girip symfony kurulumu yapacağız.

![Uygulama Ekran Görüntüsü](https://img.onl/TEfXr)


# Symfony Kurulumu

```bash
  docker exec -it ae43f14c631e bash
```
komutu ile container içine girdik. Burada `composer create-project symfony/skeleton:"6.1.*" .` komutu ile symfony'i kuralım. 

Ardından maker paketini aşağıdaki komut ile kurup, kurulum işlemini tamamlayalım

`composer require symfony/maker-bundle --dev`


# Sonuç
[http://127.0.0.1:8080](http://127.0.0.1:8080/) veya 
[http://localhost:8080](http://localhost:8080/)  adresi ile erişim sağlayabilirsiniz.


![Uygulama Ekran Görüntüsü](https://img.onl/556Fbi)
