

Novosti
=======


2.1.4 (09.03.23)
****************

**POPRAVLJENO**

- Dodane kontrole podatkov o poslovnih subjektih pri izvozu elaborata


2.1.3 (26.01.23)
****************

**NOVO**

- Dodano leto gradnje v orodje za atributiranje

**ELEKTRONSKE KOMUNIKACIJE**

- Popravki pri dodajanju kabla od začetne do končne točke
- Popravki pri izvozu elaborata


2.1.1 (04.01.23)
****************

**POPRAVLJENO**

- Popravek pri uvozu višin za pripis novo dodanim linijam


2.1.0 (23.12.22)
****************

**ELEKTRONSKE KOMUNIKACIJE**

- Možnost dodajanja cevi za označene linije za podan premer
- Možnost upoštevanja tudi nespremenjenih cevi in tras pri dodajanju kablov
- Razbijanje cevi na izbranem območju upošteva vse cevi razen brisanih


2.0.0 (29.12.22)
****************

Večja posodobitev z dodanim glavnim menijem in podporo za nov oddajni format.

**NOVO**

- Dodan glavni meni (Lastnosti, Novosti, Iskanje, Pomoč)
- Podpora novemu oddajnemu formatu (GeoJSON, JSON)
- Zapis datuma izvoza v podatke

**POPRAVLJENO**

- Prenos vseh atributov na nove linije pri razbijanju
- Optimizacija postopkov pri uvozu GURS podatkov

**ELEKTRONSKE KOMUNIKACIJE**

- Nove možnosti (vrsta kabla, število vodov, premer cevi) pri dodajanju kabla od začetne do končne točke omrežja


Starejše verzije
****************

1.13.4

- interni popravki


1.13.0

- EL-KOM svoj postopek za generiranje Hišnih priključkov ki ima sedaj parameter območje obdelave in možnost
upoštevanja tudi nespremenjenih linij


1.12.2

- popravek pri orodju za snapanje


1.12.0

- dodan postopek za razbijanje linij glede na izbran točkovni sloj


1.11.0

- podpora za GJI poligonske sloje
- poprava orodja za snap


1.10.5

- pri uvozu višin dodana možnost natančnost Z


1.10.3

- postopek za atributiranje pripiše tudi Z koordinato točkam na podlagi višine loma linije če obstaja


1.10.0

- dodan postopek za paketno atributiranje elementov
- interne optimizacije


1.9.3

- interni popravki


1.9.2

- EL-KOM (dodajanje cevi za izbrane linije)


1.9.0

- dodana orodja za EL-KOM (generiranje kablov za hišne priključke in preostale linije/cevi)


1.8.2

- interni popravki


1.8.1

- dodan lokalni linijski sloj, ki se naloži ob zagonu plugina


1.8.0

- podpora različnim vrstam GJI
- upoštevanje več polj GJI strukture (če obstajajo) pri uvozu linij in točk
- možnost dodajanja polja meril pri uvozu linij
- popravek pri brisanje stavb na GEO-PORTALu (odmik 3m)


1.7.1

- interni popravek


1.7.0

- dodan postopek za generiranje cevi glede na dogovorjen zapis v polju opis na linijah
pri razbijanju linij na območju dodana možnost razbijanja še cevi po posameznih trasah
manjši interni popravki


1.6.2

- popravki pri "Snap" postopku in pri obravnavi višin


1.6.0

- dodan postopek za uvoz GURS-ovih podatkov glede na podano razdaljo ("Buffer") od novih linij
- dodan postopek za "Snap" lomnih točk starih linij na novo dodane točke
- postopek za uvoz linij upošteva tudi polje ATR1, če obstaja


1.5.0

- dodan postopek za generiranje hišnih priključkov (HP) in preračun omrežja (network)
- uvoz dobi opcijo brisanja elementov, ki ne obstajajo več na GURS-u


1.4.0

- postopek za višine vsebuje tudi možnost upoštevanja geoida


1.3.3

- interni popravek zaradi novega strežnika


1.3.2

- možen uvoz 2D tras, popravek pri uvozu točk


1.3.1

- dodana možnost vpisa traserja pri prenosu linij na GEO-PORTAL


1.3.0

- dodan postopek za uvoz višin za 2D trase v elaboratu,
- dodan postopek za pridobitev višine iz LiDARJA za poljubno točko,
- poprava pri prenosu linij na GEO-PORTAL,
- poprava pri pridobivanju višin iz LiDARJA


1.2.1

- dodan postopek za prenos označenih linij v GEO-PORTAL trase


1.2.0

- dodan postopek za razbijanje linije na točki


1.1.2

- uskladitev z interno spremembo na bazi


1.1.1

- upoštevanje različne velikosti črk pri poljih za uvoz točk in linij


1.1.0

- uvoz posnetih točk, poprava pri uvozu linij


1.0.0

- začetna verzija
