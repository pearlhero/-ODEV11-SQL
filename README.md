# -ODEV11-SQL
dvdrental sorgu senaryoları çözümleri
Sorgu 1- actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
Çözüm 1- (SELECT first_name FROM actor)
UNION ALL
(SELECT first_name FROM customer);
<img width="509" alt="Ekran Resmi 2023-03-09 12 01 12" src="https://user-images.githubusercontent.com/116847744/223972349-733ab5f8-4514-452e-8455-a30df779ae3d.png">

Sorgu 2- actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
Çözüm 2- (SELECT first_name FROM actor)
INTERSECT
(SELECT first_name FROM customer);
<img width="520" alt="Ekran Resmi 2023-03-09 12 02 48" src="https://user-images.githubusercontent.com/116847744/223972628-dafa4962-392c-45bf-91f8-4aff10c19e66.png">

Sorgu 3- actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
Çözüm 3- (SELECT first_name FROM actor)
EXCEPT
(SELECT first_name FROM customer);
<img width="513" alt="Ekran Resmi 2023-03-09 12 03 26" src="https://user-images.githubusercontent.com/116847744/223972789-27b48662-2e47-46d3-bda7-cf6dd3723c9c.png">

Sorgu 4- İlk 3 sorguyu tekrar eden veriler için de yapalım.
Çözüm 4- (SELECT first_name FROM actor)
UNION
(SELECT first_name FROM customer);

(SELECT first_name FROM actor)
INTERSECT ALL
(SELECT first_name FROM customer);

(SELECT first_name FROM actor)
EXCEPT ALL
(SELECT first_name FROM customer);
