

Uvod
=======

GJI Elaborat omogoča izdelavo elaboratov sprememb za vpis v Zbirni kataster GJI za vse vrste infrastrukture. Deluje kot vtičnik ("plugin")
za programski paket :ref:`qgis`, podatki pa so shranjeni v relacijski podatkovni bazi, kjer so preko standardnih oblačnih storitev dostopni uporabnikom.


Značilnosti
-----------

- Pripravljen QGIS projekt za posamezno vrsto infrastrukture
- Večuporabniški dostop
- Različna orodja za vnos in paketno obdelavo podatkov
- Uvoz začetnega stanja iz evidence ZK GJI na GURS-u
- Uvoz lokalnih (terenskih) podatkov
- Samodejna določitev ID upravljavca novim elementom
- Samodejna pretvorba in obravnava GURS-ovih identifikatorjev (EID <-> ID)
- Samodejna obravnava obstoječih podatkov GURS ob spremembi (brisanje, spreminjanje)
- Samodejne vrednosti glede na nastavitve
- Uporaba šifrantov GJI
- Vsi elementi so 3D
- Enostavna kontrola in urejanje višin (možnost uporabe podatkov LiDAR)
- Kontrole in poročila
- Iskalnik
- Izvoz elaborata sprememb za oddajo na GURS (skladno z novim GeoJSON/JSON formatom)
- Redno posodabljanje aktualnega stanja ZK GJI
- Beleženje časa kreiranja, zadnje spremembe in izvoza za vsak element
- Redno arhiviranje podatkov
- Možnost prikazovanja podatkov na `GEO-PORTAL-u <https://site.geo-portal.si>`_


Komu je namenjen
----------------

GJI Elaborat je namenjen vsem, ki se ukvarjajo z vodenjem in evidentiranjem gospodarske javne infrastrukture (GJI) ter pripravo elaboratov za vpis sprememb
v zbirni kataster GJI.

Geodetska podjetja
~~~~~~~~~~~~~~~~~~

Geodetska podjetja s pooblaščenim inženirjem s področja geodezije, ki so pooblaščena s strani upravljavcev infrastrukture za izdelavo in oddajo elaboratov na
Geodetsko upravo. Za posamezno naročilo se pripravi ločen projekt, kamor je možno uvoziti posamezne meritve ter obstoječe podatke zbirnega katastra in v nekaj korakih
pripraviti elaborat za oddajo.

Upravljavci GJI in Izvajalci GJS
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    - Komunalna podjetja
    - Občine (režijski obrati)
    - Državne institucije ki upravljajo z GJI
    - Podjetja za distribucijo električne energije, zemeljskega plina, toplotne energije
    - Telekomunikacijska podjetja

GJI Elaborat omogoča povezavo z operativnim katastrom posameznega upravljavca in enostaven prenos podatkov za izdelavo elaborata sprememb za oddajo.

.. important::
 Za vsako matično številko upravljavca se v postopku izvoza ustvari ločen elaborat. Tako lahko večji uporabniki, ki zagotavljajo gospodarsko javno službo (GJS)
 na območju različnih upravljavcev (občin) v enem koraku izdelajo vse potrebne elaborate! Podrobnosti se nahajajo v poglavju: :ref:`izvoz`.

.. important::
 Povezava poteka izključno preko identifikatorjev upravljavca, kar pomeni da upravljavcu ni potrebno v lastne evidence uvažati GURS-ovih identifikatorjev in pa
 posebej voditi spremenjenih objektov. Za vse objekte se ob prenosu izvaja primerjava z aktualnim stanjem GJI.
 Podrobnosti se nahajajo v poglavju: :ref:`uvoz`.


Posebna obravnava
-----------------

Posebnosti posameznih vrst gospodarske infrastrukture, ki jih podpira GJI Elaborat so podane v nadaljevanju.

Vodovod
~~~~~~~
    - Posebnost stikanja sekundarnih in terciarnih vodov. Splošno pravilo GJI je, da morajo biti vse linije na stikih razdeljene, razen v
      primeru Vodovoda, ko se terciarni vod stika s sekundarnim. V tem primeru senkundarnega voda ni potrebno razdeliti (razbijati) na posamezne linije.
      Ta posebnost je upoštevana v postopku Razbijanja linij na določenem območju (poglavje :ref:`delo`).
    - Hišni priključki, ki so v lasti fizičnih oseb se vpišejo z matično številko 9999999 in z atributom GJI = druga infrastruktura.
      Kontrola matičnih številk upošteva to posebnost (poglavje :ref:`izvoz`).

Kanalizacija
~~~~~~~~~~~~
    - Hišni priključki, ki so v lasti fizičnih oseb se vpišejo z matično številko 9999999 in z atributom GJI = druga infrastruktura.
      Kontrola matičnih številk upošteva to posebnost (poglavje :ref:`izvoz`).

Elektronske komunikacije
~~~~~~~~~~~~~~~~~~~~~~~~

    Dodatna obravnava vseh posebnosti Elektronskih komunikacij v strukturi GJI (cevi, kabli, vodi). Uporaba omrežja za določanje tras
    za vnose kablov od začetne do končne točke.

    - Generiranje hišnih priključkov (HP) glede na trase
    - Enostavna določitev pripadajočih HP posameznim omaricam
    - Generiranje kablov za vse hišne priključke (kabel poteka po vseh trasah/ceveh od hišnega priključka do omarice)
    - Različni drugi načini generiranja cevi/kablov in pripadajočih vodov


Brezplačen preizkus
---------------------

Za brezplačen 30 dnevni preizkus vtičnika nas `kontaktirajte <https://level2.si/contact/?podrocje=gji-plugin>`_.


Razvoj in podpora
-----------------

GJI Elaborat je produkt podjetja `Level2, Uroš Preložnik s.p. <https://level2.si>`_

Uporabnikom je na voljo podpora po telefonu in e-pošti.