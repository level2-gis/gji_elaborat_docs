

Začetek dela
============

.. _qgis:

QGIS
----

Namestitev
~~~~~~~~~~

Za delo potrebujemo nameščeno aplikacijo QGIS. Gre za zelo zmogljivo in široko uporabno odprtokodno GIS aplikacijo.

`QGIS uradna stran <https://qgis.org/en/site/>`_

.. note::
 Priporoča se uporabo zadnje **LTR ("Long term release")** različice aplikacije. Nova LTR različica izide vsako leto, okvirno konec februarja.
 Minimalna zahtevana verzija je **3.16**.

Navodila za uporabo
~~~~~~~~~~~~~~~~~~~

Na voljo samo v tujih jezikih!

`Angleščina <https://docs.qgis.org/latest/en/docs/user_manual/index.html>`_

Nekaj pomembnejših poglavij za delo z vtičnikom:

- `GUI <https://docs.qgis.org/latest/en/docs/user_manual/introduction/qgis_gui.html>`_
- `Working with the Attribute Table <https://docs.qgis.org/latest/en/docs/user_manual/working_with_vector/attribute_table.html>`_
- `Editing <https://docs.qgis.org/latest/en/docs/user_manual/working_with_vector/editing_geometry_attributes.html>`_


Priprava
~~~~~~~~

.. warning::
 Aplikacija QGIS je samo delno prevedena v slovenščino. V teh navodilih se navaja angleški izraz za ukaze v QGIS uporabniškem vmesniku.

.. note::
 Uporabniški vmesnik vtičnika pa je namenjen izključno za slovenske uporabnike in je posledično v slovenskem jeziku.

Ob začetku dela je potrebno aktivirati del za obdelavo prostorskih podatkov ("Processing framework"), ki je nameščen kot osnovni vtičnik ("Plugin") ampak na začetku ni aktiviran.

Postopek:

#. Meni :menuselection:`Plugins --> Manage and install plugins...`
#. Izbira :guilabel:`Installed` zavihka na levi strani
#. Poiščite in vklopite izbiro pri zapisu |processingAlgorithm| :guilabel:`Processing`
#. Zaprite okno.


Projekt
-------

Naročnik prejme za vsak predviden elaborat za vpis sprememb v zbirni kataster GJI svoj QGIS projekt. Sloji v projektu so nastavljeni
za izbrano vrsto infrastrukture. Tipično pa so v projektu naslednji sloji in skupine:

ELABORAT V PRIPRAVI
~~~~~~~~~~~~~~~~~~~

Ta skupina prikazuje podatke, ki so novo dodani ali uvoženi iz GJI baze za namene popravljanja oz. brisanja. Sloji **Točke**, **Linije** in **Poligoni**
so na voljo za urejanje. Ob prevzemu projekta so vsi ti sloji prazni.

Skupina **POROČILA IN KONTROLE** vsebuje skupne podatke o trenutnem stanju elaborata (skupna dolžina glede na razne kriterije,...) in koristne kontrolne
sloje za opozorilo in pregled pred oddajo (Manjkajoče višine, podvojeni elementi,...)

.. note::
 Določeni sloji imajo več nastavljenih stilov risanja. Pregled stilov in menjava:

 #. Desni gumb miške na sloju v legendi
 #. Meni :menuselection:`Styles --> NAZIV STILA`

 .. image:: img/styles2.png


ELABORAT ODDAJA
~~~~~~~~~~~~~~~

Sloji v tej skupini prikazujejo v uradni strukturi GJI formata samo elemente, ki bodo del elaborata (dodani, spremenjeni, brisani). Slojev v tej skupini ni
možno urejati neposredno. Prikaz je dinamičen in se takoj osveži ob urejanju slojev v skupini **ELABORAT V PRIPRAVI**.


GJI BAZA
~~~~~~~~

Sloji v tej skupini prikazujejo trenutno stanje podatkov zbirnega katastra GJI za izbrano vrsto infrastrukture in za določene upravljavce. Tudi slojev v tej skupini ni
možno urejati neposredno. Služijo samo za prikaz, podatki iz GJI baze se v elaborat uvozijo s postopki v skupini :ref:`uvoz`.


Ostali sloji
~~~~~~~~~~~~

Ostali sloji (hišne številke, stavbe, občine, ortofoto posnetki) so namenjeni za iskanje pravih lokacij in kot pomoč pri orientaciji v prostoru.


Sloji uporabnika
~~~~~~~~~~~~~~~~

Uporabniki lahko v projekt poljubno dodajajo svoje sloje. Podatki iz uporabniških slojev se v elaborat uvozijo s postopki v skupini :ref:`uvoz`.


Vtičnik
-------

Naročniki prejmejo navodila po e-pošti za dodajanje repozitorija in namestitev ter posodabljanje vtičnika.

.. note::
 Vtičnik se uporablja vedno skupaj z QGIS projektom!

Delo z vtičnikom se deli na naslednje sklope:

- :ref:`meni`
- :ref:`urejanje`
- :ref:`orodja`

.. |processingAlgorithm| image:: /_static/common/processingAlgorithm.png
   :width: 1.5em
   :class: no-scaled-link