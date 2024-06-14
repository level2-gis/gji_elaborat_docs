

Novosti
=======

Kratek pregled novosti v posamezni verziji vtičnika.

.. _v2.6.0:

2.6.0 (14.6.24)
----------------

:newlabel:`NOVO`

- Izvoz elaborata poleg vseh potrebnih datotek, pripravi še arhivirano (ZIP) datoteko za oddajo na GURS

:fixlabel:`POPRAVLJENO`

- Izvoz elaborata sedaj pravilno zapiše število decimalnih mest v geojson datoteki v primeru QGIS 3.32 ali novejše verzije
- Orodje atributiranja sedaj določi tudi ``LETO_GRAD`` kjer je prazno, na podlagi polja ``DAT_VIR``
- Orodje za razbijanje linij na območju upošteva specifiko **vodovoda** in ne razbija **sekundarnih** vodov na stikih s **terciarnimi**
(zahtevana skripta za posodobitev baze)
- Uvoz višin upošteva polje ``ID_UPR`` če obstaja. Na ta način se na linijo povežejo samo višine z istim ``ID_UPR``.
- Pri uvozu linij ali točk je sedaj lahko ``DAT_VIR`` tudi datumsko polje (poleg teksta)

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Novo orodje za dodajanje kabla na izbrane trase
- Uvoz linij upošteva tudi specifična polja: ``PRAZNA_CEV``, ``VRSTA_KABLA``, ``ST_VODOV``
- Dodan opcijski parameter ``ID_UPR_K`` pri dodajanju kabla. V primeru da ne obstaja se kot vsi ostali ``ID_UPR`` določi samodejno.

.. _v2.5.7:

2.5.7 (20.11.23)
----------------

:fixlabel:`POPRAVLJENO`

- Poprava izvoza v primeru sprememb matičnih številk
- Poprava izvoza pri zapisu izvajalcev (MAT_GJS) v datoteko udeležencev

.. _v2.5.6:

2.5.6 (7.11.23)
----------------

:fixlabel:`POPRAVLJENO`

- Popravljena primerjava z bazo pri uvozu linij
- Odprava napak pri uvozu linij in točk v primeru nepopolne strukture GJI (uporaba privzetih vrednosti)

.. _v2.5.5:

2.5.5 (26.10.23)
----------------

:newlabel:`NOVO`

- Uvoz linij in točk sedaj upošteva tudi polji ``GJI`` in ``OPU`` v kolikor obstajata v vhodnih podatkih.

:fixlabel:`POPRAVLJENO`

- Umik parametra za natančnost pri uvozu višin (ni več potreben, saj višinske točke v novem formatu nimajo več lastnega podatka o natančnosti)
- Iz naziva za Uvoz linij in točk umaknjena beseda "novih", saj je možno uvažati tudi spremembe elementov

.. _v2.5.4:

2.5.4 (20.10.23)
----------------

:newlabel:`NOVO`

- Uvoz linij in točk sedaj upošteva tudi polja ``ID_UPR``, ``NAT_Z``, ``MAT_ST``, ``MAT_GJS`` in ``LETO_GRAD`` v kolikor obstajajo v vhodnih podatkih. V primeru obstoja ``ID_UPR`` se izvede kontrola in primerjava z bazo. Če ne obstaja v bazi, se element uvozi kot nov (D), če obstaja in v primeru razlike v podatkih ali geometriji pa se spremeni (S). Dodatno se v tem postopku uvozi tudi brisanje elementov, če obstaja ``ID_UPR`` in polje ``TIP_SPR``, ki vsebuje vrednost B.

:fixlabel:`POPRAVLJENO`

- Dodan zapis Z koordinate točkam, če jo imajo v polju Z v postopku atributiranja
- Dodano opozorilo o uvozu "Multipart" sloja v postopku kontrole točk (LiDAR)

.. _v2.5.1:

2.5.1 (06.10.23)
----------------

:newlabel:`NOVO`

- Dodano novo orodje za napenjanje poljubnega linijskega sloja na 3D na osnovi podatkov DMR

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Dodano opozorilo pri uvozu podatkov v primeru nepopolno uvoženih elementov vezanih na trase
- Poprava pri izvozu elaborata na disk

.. _v2.4.5:

2.4.5 (07.08.23)
----------------

:fixlabel:`POPRAVLJENO`

- Podpora novemu oddajnemu formatu 1.5
- Interne spremembe zaradi nove uvozne strukture podatkov GJI

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Popravek pri izračunu polj ``DIM_YX`` in ``DIM_Z`` glede na število kablov in dimenzije cevi v postopku atributiranja
- Interne optimizacije baze

.. _v2.4.4:

2.4.4 (09.05.23)
----------------

:fixlabel:`POPRAVLJENO`

- Pravilen zapis šumnikov pri izvozu v datoteko ``udelezenci.json``

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Zapis dodatnih matičnih številk pri izvozu v datoteko ``udelezenci.json`` če so določene na ceveh, kablih ali vodih

.. _v2.4.3:

2.4.3 (03.05.23)
----------------

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Postopek atributiranja sedaj pri določitvi polj ``DIM_YX`` in ``DIM_Z`` upošteva vse linije razen brisanih (prej samo D in S). Spremembo pa izvede samo v primeru, da je nova dimenzija na podlagi števila in dimenzije cevi in kablov večja od podatkov obstoječe linije.

.. _v2.4.2:

2.4.2 (25.04.23)
----------------

:newlabel:`NOVO`

- Uvoz elaborata sedaj podpira tudi nov GeoJSON format

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Novo orodje za dodajanje kabla po izbranih ceveh. Cevi morajo tvoriti eno linijo in ne smejo biti podvojene.
- Spremembe začetnih nastavitev pri nekaterih orodjih

:fixlabel:`POPRAVLJENO`

- Kontrola koordinatnega sistema pri uvozu slojev

.. _v2.3.1:

2.3.1 (17.04.23)
----------------

:newlabel:`NOVO`

- Izvoz projekta v več elaboratov hkrati. Podrobnosti: :ref:`izvoz`

.. _v2.2.0:

2.2.0 (12.04.23)
----------------

:newlabel:`NOVO`

- Dodano orodje za uvoz elaborata iz mape na disku

:fixlabel:`POPRAVLJENO`

- Izpis izvoznih JSON datotek v lepše berljivi obliki ("prettify")
- Interni popravki

.. _v2.1.4:

2.1.4 (09.03.23)
----------------

:fixlabel:`POPRAVLJENO`

- Dodane kontrole podatkov o poslovnih subjektih pri izvozu elaborata

.. _v2.1.3:

2.1.3 (26.01.23)
----------------

:newlabel:`NOVO`

- Dodano leto gradnje v orodje za atributiranje

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Popravki pri dodajanju kabla od začetne do končne točke
- Popravki pri izvozu elaborata

.. _v2.1.1:

2.1.1 (04.01.23)
----------------

:fixlabel:`POPRAVLJENO`

- Popravek pri uvozu višin za pripis novo dodanim linijam

.. _v2.1.0:

2.1.0 (23.12.22)
----------------

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Možnost dodajanja cevi za označene linije za podan premer
- Možnost upoštevanja tudi nespremenjenih cevi in tras pri dodajanju kablov
- Razbijanje cevi na izbranem območju upošteva vse cevi razen brisanih

.. _v2.0.0:

2.0.0 (29.11.22)
----------------

Večja posodobitev z dodanim glavnim menijem in podporo za nov oddajni format.

:newlabel:`NOVO`

- Dodan glavni meni (Lastnosti, Novosti, Iskanje, Pomoč)
- Podpora novemu oddajnemu formatu (GeoJSON, JSON)
- Zapis datuma izvoza v podatke

:fixlabel:`POPRAVLJENO`

- Prenos vseh atributov na nove linije pri razbijanju
- Optimizacija postopkov pri uvozu GURS podatkov

:elkomlabel:`ELEKTRONSKE KOMUNIKACIJE`

- Nove možnosti (vrsta kabla, število vodov, premer cevi) pri dodajanju kabla od začetne do končne točke omrežja


Starejše verzije
----------------

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
