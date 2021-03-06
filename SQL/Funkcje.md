# Funkcje

## Łączenie się z tabelą za pomocą innych id
``` sql
SELECT *
FROM `tab1`
JOIN `tab2` on `tab2_id` = `tab1_id`
```


## Tekstowe
`COINCAT(pole1, pole2, pole3)` -> "pole1pole2pole3"
	łączy znaki z pul

`CONCAT_WS(" ",pole1, pole2, pole3)` -> "pole1 pole2 pole3" łączy znaki z pul rozdzielając znakiem (w tym przypadku spacja)

`LOWER("aBcD")` -> "abcd"

`UPPER("aBcD")` -> "ABCD"

`LEFT(Rekord, ile)` / `RIGHT(Rekord, ile)`
z rekordu bierze podaną ilość znaków z lewej/prawej strony

`TRIM(" Usuwa spacjje z krawędzi ")` -> "Usuwa spacjje z krawędzi"

`INSTR("ABCD", "C")` -> 3

`REPLACE("ABCD", "C", "J")` -> "ABJD"

`REVERSE("ABCD")` -> "DCBA"

`SUBSTRING("ABCDEFGH", 3, 2)` -> "CD"
Od trzeciego znaku bierze wypisuje 2 znaki

`LENGTH("ABCD")` -> 4

## Liczbowe
`ROUND("123.456", 2)` -> 123.46

`ROUND("123.456", -2)` -> 100

`ABS(2)` -> 2

`ABS(+2)` -> 2

`ABS(-2)` -> 2

`POW(2, 3)` -> 8 (2^3)

`POW(4, (1/2))` -> 2	(4^(1/2))

`SQRT(4)` -> 2	Pierwiastek TYLKO z dwóch

`MOD(7,2)` -> 1	Reszta z dzielenia

## Data i czas
`CURDATE()` - aktualny data (rrrr-mm-dd)

`CURTIME()` - aktualny czas (hh:mm:ss)

`NOW()` - aktualan data i czas (rrrr-mm-dd hh:mm:ss)

`DAYOFWEEK("2017-09-19")` -> 3 (1=Niedziela, 2=Poniedziałek, 3=Wtore, ..., 7=Sobota)

`DAYOFMONTH("2017-09-19")` -> 19

`DAYOFYEAR("2017-09-19")` -> 262

`YEAR("2017-09-19")` -> 2017

`MONTH("2017-09-19")` -> 9

`DAY("2017-09-19")` -> 19

`HOUR("21:37:16")` -> 21

`MINUTE("21:37:16")` -> 37

`SECOND("21:37:16")` -> 16


Mozliwe łączenie np `DAYOFWEEK(NOW())`

## Szyfry
`ENCODE()` - szyfruje

`DECODE()` - odszyfrowuje to co wyżej

`SHA1()` / `PASSWORD()` - szyfrujje bez możliwości odszyfrowania