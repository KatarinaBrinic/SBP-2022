# SBP-2022 (Projekat iz sistema baza podataka)

Tema: Analiza spotify numera kroz playliste i njihove atribute 

Autori: Kristina Todić IN58/2018, Katarina Brinić IN43/2018

Opis skupa podataka
Za potrebe projekta korištena su dva skupa podataka:

Skup podataka o pesmama
Skup sadrži podatke o top100 pesama prikupljene sa Spotify-a. Korištena je datoteka iz skupa sa osnovnim informacijama o pesmama (songs.csv). Detaljniji opis podataka sadržanih u skupu može se pronaći u predlogu projekta.
Skup podataka o playlistama sa Spotify-a
Skup podataka je uključuje detalje o autoru playliste, imenu autora pesme koja se nalazi na playlisti kao i naslovu same pesme i na kraju nazivu playliste.Veličina inicijalnog skupa podataka je oko 2gb. 
Rezultati
Šeme baze podataka
Kreirane su dve šeme baze podataka, dok je glavni cilj pri kreiranju druge šeme bio poboljšanje performansi upita.

Opis inicijalne šeme dostupan je u v1/schema. Za upis podataka iz skupa podataka u bazu korištena je Python skripta, koja se zajedno sa uputstvom za pokretanje nalazi u v1/scripts.

Druga šema baze podataka kreirana je transformacijom prve šeme, uz upotrebu šablona baketiranja. Detaljan opis druge šeme dostupan je u v2/schema, a skripta za kreiranje šeme sa uputstvom za pokretanje u v2/scripts.

Upiti
1. Koliko puta se desilo da najpopularnija (popularity veci i jednak od 88) pesma nije u top3? 
2. Pronaći da li se pesme izvođača nalaze i u ostalih top100 (bez top1) i koliko puta.
3. Koji su faktori top5 pesama u 2010. godini?
4. Na koliko playlisti se nalaze top1 pesme?
5. Pronaći prosečan broj playlisti na kojima se nalaze izvođači top1 pesama.
6. Za svaki žanr odrediti pesmu sa najvećom popularnošću. 
7. Na osnovu prethodne agregacije odrediti kojih godina je popularnost određenog žanra bila najveća, pa na osnovu pomenutog uporediti “popularnost” žanrova kroz godine. 
8. Uporediti pesme kroz top50 sa najvećom danceability i loudness (interesuje nas kolika je korelacija ova 2 faktora).
9.  Pronaći top10 pesama sa najvećom popularnošću i uporediti ih sa liveness atributom (interesuje nas koliko pesama od top10 ima bolju verziju uživo).
10. Pronaći prosječan broj playlisti na kojima se nalaze izvođači top3 pjesme.

Performanse
Procjena performansi izvršena je pomoću metode explain("executionStats") koju nudi MongoDB. Grafici prikazuju izmereno vreme izvršavanja upita nad prvom i drugom verzijom baze.

