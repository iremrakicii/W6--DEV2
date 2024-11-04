# SQL Sorgu Örnekleri

Bu dosya, SQL dilinde belirli veri sorgulama örneklerini içermektedir. Sorgular, belirli koşullara göre veri filtreleme, belirli sütunları seçme ve birden fazla koşul uygulama gibi SQL'in temel özelliklerini göstermektedir.

## Sorgular ve Açıklamaları

### 1. Replacement Cost’a Göre Film Seçimi
Bu sorgu, `replacement_cost` (yenileme maliyeti) değeri 12.99 ile 16.99 arasında olan filmleri seçer.

```sql
SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 AND 16.99;
Tablo: film
Koşul: replacement_cost değeri 12.99 ile 16.99 arasında olan kayıtları seçer.
```
### 2. Belirli İsimlere Göre Aktör Seçimi
Bu sorgu, adı Penelope, Nick veya Ed olan aktörlerin ad ve soyad bilgilerini getirir.

```sql
SELECT first_name, last_name FROM actor
WHERE first_name IN ('Penelope', 'Nick', 'Ed');
Tablo: actor
Koşul: first_name değeri belirtilen isimlerden biri olan kayıtları seçer.
```
### 3. Rental Rate ve Replacement Cost'a Göre Film Seçimi
Bu sorgu, rental_rate değeri 0.99, 2.99 veya 4.99 ve replacement_cost değeri 12.99, 15.99 veya 28.99 olan filmleri getirir.

```sql
SELECT * FROM film
WHERE (rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99));
Tablo: film
Koşul: Hem rental_rate hem de replacement_cost belirtilen değerlerde olan kayıtları seçer.
```
