1. Wstęp
Zadanie polegało na zaprojektowaniu modeli relacyjnych dla różnych typów związków, takich jak: monogamia, poligamia, poliandria oraz małżeństwo grupowe. Każdy z tych związków został przedstawiony za pomocą diagramu ERD (Entity-Relationship Diagram), a relacje pomiędzy encjami odzwierciedlają różne rodzaje związków rodzinnych.

2. Opis modeli
2.1. Monogamia
Monogamia to związek, w którym jeden mężczyzna pozostaje w związku z jedną kobietą. W bazie danych jest to przedstawione jako relacja jeden-do-jednego (1:1). W modelu mamy dwie tabele: Mezczyzni i Kobiety, gdzie mężczyzna ma klucz obcy (Kobiety_idKobiety) wskazujący na tabelę kobiet, co odzwierciedla relację między nimi.

Mezczyzni:

idMezczyzni (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Kobiety_idKobiety (klucz obcy)
Kobiety:

idKobiety (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
2.2. Poligamia
W poligamii jeden mężczyzna może być związany z wieloma kobietami, co oznacza relację jeden-do-wielu (1
). W bazie danych mężczyzna ma klucz obcy do tabeli kobiet, która pozwala na przypisanie wielu kobiet do jednego mężczyzny.

Mezczyzni:

idMezczyzni (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Kobiety:

idKobiety (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Mezczyzni_idMezczyzni (klucz obcy)
2.3. Poliandria
Poliandria to związek, w którym jedna kobieta jest związana z wieloma mężczyznami. Jest to odwrotność poligamii i jest przedstawiona za pomocą relacji wiele-do-jednego (N:1), gdzie wielu mężczyzn może być powiązanych z jedną kobietą.

Mezczyzni:

idMezczyzni (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Kobiety2_idKobiety (klucz obcy)
Kobiety:

idKobiety (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
2.4. Małżeństwo grupowe
W małżeństwie grupowym zarówno wielu mężczyzn, jak i wiele kobiet może być powiązanych ze sobą. Jest to relacja wiele-do-wielu (N
), co oznacza, że wymaga dodatkowej tabeli pośredniej, która przechowuje klucze główne z obu tabel.

Mezczyzni:

idMezczyzni (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Kobiety:

idKobiety (klucz główny)
imie
nazwisko
dataUrodzenia
adres
inneDane
Mezczyzni_has_Kobiety (tabela pośrednia):

Mezczyzni_idMezczyzni (klucz obcy z tabeli Mezczyzni)
Kobiety_idKobiety (klucz obcy z tabeli Kobiety)
3. Wnioski
Projektowanie relacji bazodanowych dla różnych modeli związków wymaga odpowiedniego rozróżnienia relacji jeden-do-jednego, jeden-do-wielu oraz wiele-do-wielu. Każdy model związków ma swoje unikalne wymagania dotyczące struktury tabel oraz kluczy obcych, co wpływa na sposób przechowywania danych i ich spójność.

