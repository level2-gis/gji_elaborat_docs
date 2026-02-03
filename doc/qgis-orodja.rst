
.. _qgis-orodja:

Izbrana QGIS orodja
===================

Opisana so nekatera standardna orodja, ki so vključena v QGIS in jih potrebujemo pri delu z vtičnikom. Orodja so del
"Processing Toolbox"-a (meni :menuselection:`Processing --> Toolbox`), kjer so razdeljena v več skupin. Najlažje jih poiščemo z iskalnikom.

.. figure:: img/searchtools.png

   Iskanje orodja

Extract vertices
----------------

Orodje na podlagi vhodnega linijskega ali poligonskega sloja izdela točkovni sloj vseh lomnih točk sloja. Primerno za
določitev ali kontrolo višin z uporabo orodja :ref:`kontrola_lidar`

Refactor fields
----------------

Orodje omogoča spremembo imen in drugih lastnosti podatkovne tabele izvornega sloja. Spremembe se zapišejo v novem sloju.
Uporabno pred uvozom podatkov v elaborat, kjer želimo uskladiti imena in lastnosti polj glede na strukturo baze: :ref:`struktura`.
Na ta način zagotovimo uvoz vseh pomembnih opisnih podatkov našega izvornega sloja.

.. figure:: img/refactor_fields.png

   Polja izvornega sloja imamo na levi strani, polja željene strukture lahko naložimo iz poljubnega sloja, nato jih uskladimo
   in prilagodimo po želji.

.. _setz:

Set Z value
-----------

Orodje izbranemu točkovnemu sloju določi Z vrednost, tako da je rezultat 3D sloj (koordinate so zapisane v obliki X,Y,Z). Tipično se določi Z vrednost na podlagi vrednosti v določenem polju.

.. figure:: img/setz1.png

   Za določitev Z na podlagi vrednosti polja, uporabimo dodatne možnosti

.. figure:: img/setz2.png

   Nato izberemo :menuselection:`Field type... --> [IME POLJA]`

3D točkovni sloj potrebujemo pri uvozu točk in višin ter kadar rišemo novo 3D linijo na podlagi 3D točk.