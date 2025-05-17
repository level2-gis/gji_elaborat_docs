
.. _struktura:

Podatkovna struktura
====================

Struktura tabel v bazi za izdelavo GJI elaborata sledi prejšnjemu formatu Geodetske uprave (GURS) z upoštevanjem sprememb
novega GeoJSON formata. Vsebuje pa še nekatera dodatna polja vezana na delovišče in naročnikove podatke ter različna
sistemska polja.

.. csv-table:: Struktura posamezne tabele
    :file: _static/struktura.csv
    :header-rows: 1
    :delim: ;

Pri linijah pa lahko vodimo še dodatne atribute kot so: ``MERIL``, ``TRASIRAL`` in ``SIFRA_PROJEKTA``.

Geometrija v vseh tabelah je 3D (PointZ, LineStringZ, MultiPolygonZ).