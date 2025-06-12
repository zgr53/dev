# E-Ticaret Demo Uygulaması

Bu proje, temel bir e-ticaret backend API'sidir. Java, Spring Boot, H2 veritabanı ve Maven kullanılmıştır. Proje, ürün, kullanıcı ve sipariş yönetimi sağlar.

## Özellikler
- Ürün, kullanıcı ve sipariş CRUD işlemleri
- Sipariş oluştururken stok kontrolü
- H2 veritabanı ile hızlı test
- RESTful API
- Docker ile deploy edilebilir

## Çalıştırma

### Maven ile
```bash
mvn clean package
java -jar target/ecommerce-demo-1.0.0.jar
```

### Docker ile
Önce jar dosyasını üretin:
```bash
mvn clean package
```
Sonra Docker imajı oluşturup çalıştırın:
```bash
docker build -t ecommerce-demo .
docker run -p 8080:8080 ecommerce-demo
```

## API Uç Noktaları
- `/api/products` : Ürün işlemleri
- `/api/users` : Kullanıcı işlemleri
- `/api/orders` : Sipariş işlemleri

## H2 Konsolu
`http://localhost:8080/h2-console` (JDBC URL: `jdbc:h2:mem:testdb`)

## Notlar
- Proje, Java 17 ile derlenmiştir.
- Spring Boot 3.x kullanılmıştır.
- Geliştirme ve test için uygundur.