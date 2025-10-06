.. _novosti:

Novosti
=======

Kratek pregled novosti v posamezni verziji vtičnika.

.. _v2.11.2:

2.11.2 (4.10.25)
----------------

|newlabel|

- Dodano orodje za analizo in popravo spremenjenih elementov
- V glavnem meniju so dodane nastavitve vtičnika za določitev povezave z PostgreSQL bazo za pridobitev naslovov in poslovnih subjektov ter višinskih podatkov

|elkomlabel|

- Hišni priključki sedaj vsebujejo tudi polja ``VRSTA_KABLA`` in ``ST_VODOV``, ki se določita iz pripadajoče linije ter uporabita pri dodajanju
  kablov za izbrane hišne priključke ter ``NASLOV``, ki se določi v primeru da je linija hišnega priključka znotraj poligona stavbe, ki ima naslov.
  V primeru, da ima stavba več naslovov, se uporabi najbližji.

.. _v2.10.4:

2.10.4 (28.7.25)
----------------

|fixlabel|

- Izvoz elaborata sedaj izpusti pripravo datotek :file:`upravljavci.json` in :file:`izvajalci.json` v primeru prazne vsebine
  (ni novo dodanih objektov). Datoteki tudi ne vsebujeta več praznih vrednosti v sklopu ``podatki``.
- Popravek pri uvozu podatkov glede nastavitev praznih vrednosti polj ``NAT_Z``, ``ATR1``, ``ATR2`` in ``ATR3``, ki vsebujejo šifrante (``0`` namesto ``null``)
- Upoštevanje spremenjene šifre objektov pri uvozu točk in poligonov
- Orodje razbijanja linij na območju vsebuje tudi postopek brisanja podvojenih linij in osveževanje sloja prekritih linij

|elkomlabel|

- Orodje za generiranje omrežja sedaj ne vsebuje več razbijanja linij na celotnem območju. To se rešuje parcialno z
  ločenim orodjem.
- Razbijanje cevi kot opcijski parameter pri orodju razbijanja linij na območju je umaknjen. Postopek sedaj vedno razbija
  cevi, ki obstajajo na trasi, ki se z orodjem razbijanja deli.


.. _v2.10.3:

2.10.3 (15.6.25)
----------------

|fixlabel|

- Orodje za atributiranje sedaj uskladi polja ``NAT_YX`` in ``VIR`` glede na pravila GURS-a
- Pravilno osveževanje števila elementov sloja v legendi po uporabi orodja, ki spremeni število elementov
- Interna optimizacija postopka za pripis višinskih točk iz sosednjih linij, ki se uporablja v več orodjih

.. _v2.10.1:

2.10.1 (10.6.25)
----------------

|newlabel|

- Dodano orodje za brisanje podvojenih linij (zahtevana posodobitev baze)

|elkomlabel|

- Več možnosti izbora linij pri generiranju hišnih priključkov

|fixlabel|

- Brisanje podatkov o izvozu elaborata (zadeva, predmet vpisa) ob brisanju celotnega elaborata


.. _v2.9.0:

2.9.0 (29.4.25)
----------------

|newlabel|

- Dodano novo orodje za združitev in prikaz SHP slojev iz množice ZIP datotek znotraj določene mape

|fixlabel|

- Bolj pregleden izpis za uporabnika pri uvozu lastnih podatkov
- Razbijanje linij z območjem sedaj izpiše elemente, kjer razbijanje ni bilo možno ter nadaljuje postopek
- Manjši popravki pri atributiranju za nastavitve polj ``NAT_Z`` in ``Z``

.. _v2.8.5:

2.8.5 (30.12.24)
----------------

|elkomlabel|

- Dodana možnost podaljšanja kabla za izbrane cevi ali izbrane trase v okviru obstoječih orodij.
- Dodajanje kablov za izbrane hišne priključke sedaj poleg vrste voda upošteva tudi podatek števila vodov iz pripadajoče linije hišnega priključka.

.. _v2.8.3:

2.8.3 (4.11.24)
----------------

|newlabel|

- Pri uvozu višin sedaj lahko višine pripišemo tudi na poligonski sloj

|fixlabel|

- Manjši popravek pri uvozu lastnih podatkov in primerjavi z bazo
- Nekaj internih popravkov

.. _v2.8.0:

2.8.0 (13.10.24)
----------------

|newlabel|

- Novo orodje za brisanje vseh podatkov v elaboratu naenkrat in ponastavitev začetnega stanja vseh pripadajočih tabel

|fixlabel|

- Odprava napake zaradi katere vtičnik ni delal s QGIS 3.38
- Manjši popravki pri uvozu podatkov GURS, pri primerjavi z bazo pri uvozu lastnih podatkov ter pri izvozu elaborata na disk

.. _v2.7.0:

2.7.0 (24.8.24)
----------------

|newlabel|

- Uvoz poligonskega sloja v elaborat

|fixlabel|

- Nastavitev večje kompresije izvozne ZIP datoteke

.. _v2.6.0:

2.6.0 (14.6.24)
----------------

|newlabel|

- Izvoz elaborata poleg vseh potrebnih datotek, pripravi še arhivirano (ZIP) datoteko za oddajo na GURS

|fixlabel|

- Izvoz elaborata sedaj pravilno zapiše število decimalnih mest v geojson datoteki v primeru QGIS 3.32 ali novejše verzije
- Orodje atributiranja sedaj določi tudi ``LETO_GRAD`` kjer je prazno, na podlagi polja ``DAT_VIR``
- Orodje atributiranja sedaj določi tudi polje ``Z`` za točke na podlagi Z koordinate ter polja ``SIF_VRSTE`` in ``DIM_Z``
- Orodje za razbijanje linij na območju upošteva specifiko **vodovoda** in ne razbija **sekundarnih** vodov na stikih s **terciarnimi** (zahtevana skripta za posodobitev baze)
- Uvoz višin upošteva polje ``ID_UPR`` če obstaja. Na ta način se na linijo povežejo samo višine z istim ``ID_UPR``.
- Pri uvozu linij ali točk je sedaj lahko ``DAT_VIR`` tudi datumsko polje (poleg teksta)

|elkomlabel|

- Novo orodje za dodajanje kabla na izbrane trase
- Uvoz linij upošteva tudi specifična polja: ``PRAZNA_CEV``, ``VRSTA_KABLA``, ``ST_VODOV``
- Dodan opcijski parameter ``ID_UPR_K`` pri dodajanju kabla. V primeru da ne obstaja se kot vsi ostali ``ID_UPR`` določi samodejno.

.. _v2.5.7:

2.5.7 (20.11.23)
----------------

|fixlabel|

- Poprava izvoza v primeru sprememb matičnih številk
- Poprava izvoza pri zapisu izvajalcev (MAT_GJS) v datoteko udeležencev

.. _v2.5.6:

2.5.6 (7.11.23)
----------------

|fixlabel|

- Popravljena primerjava z bazo pri uvozu linij
- Odprava napak pri uvozu linij in točk v primeru nepopolne strukture GJI (uporaba privzetih vrednosti)

.. _v2.5.5:

2.5.5 (26.10.23)
----------------

|newlabel|

- Uvoz linij in točk sedaj upošteva tudi polji ``GJI`` in ``OPU`` v kolikor obstajata v vhodnih podatkih.

|fixlabel|

- Umik parametra za natančnost pri uvozu višin (ni več potreben, saj višinske točke v novem formatu nimajo več lastnega podatka o natančnosti)
- Iz naziva za Uvoz linij in točk umaknjena beseda "novih", saj je možno uvažati tudi spremembe elementov

.. _v2.5.4:

2.5.4 (20.10.23)
----------------

|newlabel|

- Uvoz linij in točk sedaj upošteva tudi polja ``ID_UPR``, ``NAT_Z``, ``MAT_ST``, ``MAT_GJS`` in ``LETO_GRAD`` v kolikor obstajajo v vhodnih podatkih. V primeru obstoja ``ID_UPR`` se izvede kontrola in primerjava z bazo. Če ne obstaja v bazi, se element uvozi kot nov (D), če obstaja in v primeru razlike v podatkih ali geometriji pa se spremeni (S). Dodatno se v tem postopku uvozi tudi brisanje elementov, če obstaja ``ID_UPR`` in polje ``TIP_SPR``, ki vsebuje vrednost B.

|fixlabel|

- Dodan zapis Z koordinate točkam, če jo imajo v polju Z v postopku atributiranja
- Dodano opozorilo o uvozu "Multipart" sloja v postopku kontrole točk (LiDAR)

.. _v2.5.1:

2.5.1 (06.10.23)
----------------

|newlabel|

- Dodano novo orodje za napenjanje poljubnega linijskega sloja na 3D na osnovi podatkov DMR

|elkomlabel|

- Dodano opozorilo pri uvozu podatkov v primeru nepopolno uvoženih elementov vezanih na trase
- Poprava pri izvozu elaborata na disk

.. _v2.4.5:

2.4.5 (07.08.23)
----------------

|fixlabel|

- Podpora novemu oddajnemu formatu 1.5
- Interne spremembe zaradi nove uvozne strukture podatkov GJI

|elkomlabel|

- Popravek pri izračunu polj ``DIM_YX`` in ``DIM_Z`` glede na število kablov in dimenzije cevi v postopku atributiranja
- Interne optimizacije baze

.. _v2.4.4:

2.4.4 (09.05.23)
----------------

|fixlabel|

- Pravilen zapis šumnikov pri izvozu v datoteko ``udelezenci.json``

|elkomlabel|

- Zapis dodatnih matičnih številk pri izvozu v datoteko ``udelezenci.json`` če so določene na ceveh, kablih ali vodih

.. _v2.4.3:

2.4.3 (03.05.23)
----------------

|elkomlabel|

- Postopek atributiranja sedaj pri določitvi polj ``DIM_YX`` in ``DIM_Z`` upošteva vse linije razen brisanih (prej samo D in S). Spremembo pa izvede samo v primeru, da je nova dimenzija na podlagi števila in dimenzije cevi in kablov večja od podatkov obstoječe linije.

.. _v2.4.2:

2.4.2 (25.04.23)
----------------

|newlabel|

- Uvoz elaborata sedaj podpira tudi nov GeoJSON format

|elkomlabel|

- Novo orodje za dodajanje kabla po izbranih ceveh. Cevi morajo tvoriti eno linijo in ne smejo biti podvojene.
- Spremembe začetnih nastavitev pri nekaterih orodjih

|fixlabel|

- Kontrola koordinatnega sistema pri uvozu slojev

.. _v2.3.1:

2.3.1 (17.04.23)
----------------

|newlabel|

- Izvoz projekta v več elaboratov hkrati. Podrobnosti: :ref:`izvoz`

.. _v2.2.0:

2.2.0 (12.04.23)
----------------

|newlabel|

- Dodano orodje za uvoz elaborata iz mape na disku

|fixlabel|

- Izpis izvoznih JSON datotek v lepše berljivi obliki ("prettify")
- Interni popravki

.. _v2.1.4:

2.1.4 (09.03.23)
----------------

|fixlabel|

- Dodane kontrole podatkov o poslovnih subjektih pri izvozu elaborata

.. _v2.1.3:

2.1.3 (26.01.23)
----------------

|newlabel|

- Dodano leto gradnje v orodje za atributiranje

|elkomlabel|

- Popravki pri dodajanju kabla od začetne do končne točke
- Popravki pri izvozu elaborata

.. _v2.1.1:

2.1.1 (04.01.23)
----------------

|fixlabel|

- Popravek pri uvozu višin za pripis novo dodanim linijam

.. _v2.1.0:

2.1.0 (23.12.22)
----------------

|elkomlabel|

- Možnost dodajanja cevi za izbrane trase za podan premer
- Možnost upoštevanja tudi nespremenjenih cevi in tras pri dodajanju kablov
- Razbijanje cevi na izbranem območju upošteva vse cevi razen brisanih

.. _v2.0.0:

2.0.0 (29.11.22)
----------------

Večja posodobitev z dodanim glavnim menijem in podporo za nov oddajni format.

|newlabel|

- Dodan glavni meni (Lastnosti, Novosti, Iskanje, Pomoč)
- Podpora novemu oddajnemu formatu (GeoJSON, JSON)
- Zapis datuma izvoza v podatke

|fixlabel|

- Prenos vseh atributov na nove linije pri razbijanju
- Optimizacija postopkov pri uvozu GURS podatkov

|elkomlabel|

- Nove možnosti (vrsta kabla, število vodov, premer cevi) pri dodajanju kabla od začetne do končne točke omrežja


Starejše verzije
----------------

1.13.4

- interni popravki


1.13.0

- EL-KOM svoj postopek za generiranje Hišnih priključkov ki ima sedaj parameter območje obdelave in možnost upoštevanja tudi nespremenjenih linij


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

- dodan postopek za generiranje cevi glede na dogovorjen zapis v polju opis na linijah pri razbijanju linij na območju dodana možnost razbijanja še cevi po posameznih trasah manjši interni popravki


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

- dodan postopek za prenos izbranih linij v GEO-PORTAL trase


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
