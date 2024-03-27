# SQL_Assignment_10

## Sorgu Senaryoları

* city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.

```bash
SELECT city.city_id, city.city, country.country_id, country.country
FROM city
LEFT JOIN country ON city.country_id = country.country_id;
```



* customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.

```bash
SELECT customer.customer_id, customer.first_name, customer.last_name, payment.payment_id
FROM customer
RIGHT JOIN payment ON customer.customer_id = payment.customer_id;
```



* customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.

```bash
SELECT customer.customer_id, customer.first_name, customer.last_name, rental.rental_id
FROM customer
FULL JOIN rental ON customer.customer_id = rental.customer_id;
```

Bu sorgu, customer tablosundaki tüm müşterileri ve kiralamalarını rental tablosuyla ilişkilendirerek birlikte gösterir. FULL JOIN, customer ve rental tablosundaki tüm kayıtları döndürür, eşleşen kayıtlar varsa onları da ekler.

Not: Bu sorgularda, dvdrental örneği veri tabanında bulunan tablo ve sütun isimleri kullanılmıştır. Kendi veri tabanınızda bu sorguları çalıştırırken tablo ve sütun isimlerini kendi veri tabanınıza göre değiştirmeniz gerekmektedir.