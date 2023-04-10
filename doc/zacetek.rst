

Začetek dela
============


QGIS
----

Namestitev
~~~~~~~~~~

Za delo potrebujemo nameščeno aplikacijo QGIS. Gre za zelo zmogljivo in široko uporabno odprtokodno GIS aplikacijo.

`Prenos aplikacije <https://qgis.org/en/site/forusers/download.html>`_

.. note::
 Priporoča se uporabo **LTR ("Long term release")** različic aplikacije.
 Minimalna zahtevana verzija je **3.16**.

Navodila za uporabo
~~~~~~~~~~~~~~~~~~~

.. warning::
 Na voljo samo v tujih jezikih!

 `Angleščina <https://docs.qgis.org/3.28/en/docs/user_manual/index.html>`_

Nekaj pomembnejših poglavij pomembnih za delo z vtičnikom:

- `GUI <https://docs.qgis.org/3.28/en/docs/user_manual/introduction/qgis_gui.html>`_
- `Working with the Attribute Table <https://docs.qgis.org/3.28/en/docs/user_manual/working_with_vector/attribute_table.html>`_
- `Editing <https://docs.qgis.org/3.28/en/docs/user_manual/working_with_vector/editing_geometry_attributes.html>`_


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


Vtičnik
-------

Naročniki prejmejo navodila po e-pošti za dodajanje repozitorija in namestitev vtičnika.

Delo z vtičnikom se deli na naslednje sklope:

- :ref:`meni`
- :ref:`urejanje`
- :ref:`orodja`


Projekt
-------

V pripravi

.. |processingAlgorithm| image:: /_static/common/processingAlgorithm.png
   :width: 1.5em