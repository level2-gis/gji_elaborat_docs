
.. _urejanje:

Vnos in urejanje podatkov
=========================

Ročni vnos
-----------

Ročni vnos je primeren, kadar:

- Dodajamo linijske elemente s povezovanjem na podlagi sloja terenskih točk
- Prenašamo podatke iz načrtov ali drugih podlag iz projekta

**Postopek ročnega vnosa:**

1. Izberemo želeni sloj v zavihku **Sloji**
2. Vklopimo način urejanja sloja |mActionToggleEditing|
3. Izberemo orodje za risanje, na voljo samo eden, odvisno od geometrije sloja:
   
   - |mActionCaptureLine| **Dodaj linijski element**
   - |mActionCapturePoint| **Dodaj točkovni element**
   - |mActionCapturePolygon| **Dodaj poligonski element**

4. Kliknemo na karto za začetek risanja
5. Za linijske in poligonske elemente: nadaljujemo s kliki za lomne točke, desni klik za zaključek
6. Odpre se obrazec za vnos opisnih podatkov (atributov)
7. Izpolnimo polja
8. Potrdimo z **OK**
9. Shranimo spremembe |mActionSaveAllEdits|

.. note::
   V primeru kompleksnejše simbologije je možno, da novo dodan element ne bo viden na karti dokler ne bodo shranjene spremembe |mActionSaveAllEdits|.

.. tip::
   Kadar z linijami povezujemo terenske točke se bodo višine terenskih točk prenesle v višine lomnih točk linije. Pomembno je, da pri tem
   uporabljamo način |mIconSnapping| **Snap**.

Uvoz iz lokalnih slojev
------------------------

Kadar že razpolagamo s prostorskimi podatki v različnih formatih, ki jih lahko odpremo v QGIS-u (Shapefile, GeoPackage, DXF, itd.), lahko podatke uvozimo neposredno v GJI elaborat.
Opis postopka: :ref:`uvoz_lokalnih_slojev`.

Kopiraj & Prilepi
------------------

.. warning::
   QGIS sicer omogoča kopiranje elementov iz enega sloja in lepljenje v drugega, vendar pa tega postopka **ne moremo** uporabiti za prenos elementov v elaborat.
   Podatke prenašamo v elaborat **vedno** s postopki uvoza: :ref:`uvoz`.


Urejanje geometrije
--------------------

Urejanje geometrije elementov je opisano v uradni dokumentaciji `Editing <https://docs.qgis.org/3.40/en/docs/user_manual/working_with_vector/editing_geometry_attributes.html#editing>`_.

.. tip::
   Tipka :kbd:`F5` **Osveži** je zelo uporabna pri urejanju geometrije (lomnih točk) kadar delamo veliko sprememb, moramo ročno osvežiti podatke, da dobimo zadnje stanje lomnih točk iz baze.

Razbijanje linij
~~~~~~~~~~~~~~~~~
.. warning::
   Razbijanje linij v elaboratu **vedno** izvajamo z orodji vtičnika, glej :ref:`delo`. Podatkov v elaboratu **ne moremo** razbijati z QGIS načinom
   |mActionSplitFeatures| **Split features**.

Združevanje linij
~~~~~~~~~~~~~~~~~
.. note::
   Kadar želimo več med seboj povezanih linij združiti v eno, lahko uporabimo QGIS način |mActionMergeFeatures| **Merge selected features**,
   vendar moramo pri tem upoštevati naslednja pravila:

   1. Linije morajo biti med seboj povezane, da lahko združevanje tvori eno geometrijo
   2. Pri določevanju vrednosti polj nove linije za polja: ``gp_id``, ``gurs_id``, ``tip_spr``, ``id_upr`` pustimo **privzete vrednosti** in jih ne spreminjamo

.. warning::
   V primeru Elektronskih komunikacij, če imajo linije ki se združujejo dodatne podatke (cevi, kable) se ti podatki **ne prenesejo**
   na novo linijo z uporabo QGIS načina |mActionMergeFeatures| **Merge selected features**. Torej se brišejo!

Podvojene linije
~~~~~~~~~~~~~~~~

Urejanje geometrijsko podvojenih linij je posebej zahtevno pri **Elektronskih komunikacijah**, kjer lahko vsaka linija vsebuje ločene cevi ali kable.
Za ta namen uporabljamo orodje vtičnika za **brisanje podvojenih linij**, kjer se pripadajoči elementi linij ki se brišejo prenesejo na linije, ki ostanejo.
Postopek je vključen tudi v orodja za **razbijanje linij**, glej :ref:`delo`.

Atributno urejanje
-------------------

Atributno urejanje pomeni spreminjanje opisnih podatkov (atributov polj) elementov. Lahko spreminjamo atribute posameznim elementom
ali pa več elementom hkrati, tako da izbranim elementom določimo enake vrednosti polj v enem koraku.

**Postopek atributnega urejanja:**

.. note::
  Opisan postopek je enak ne glede na to ali spreminjamo podatke enega ali več elementov (paketno urejanje).

1. Izberemo (aktiviramo) želeni sloj v zavihku **Sloji**
2. Vklopimo način urejanja sloja |mActionToggleEditing|
3. Izberemo element(e) aktivnega sloja, tipično z izborom na karti, lahko tudi preko atributne tabele, tipka :kbd:`F6`

   .. figure:: img/qgis_select_options.png

      Možnost izbora elementov preko karte
4. Kliknemo na ikono za urejanje podatkov izbranih elementov |mActionMultiEdit| **Multi edit**
5. Na obrazcu vpišemo željene spremembe, ki se bodo pripisale vsem izbranim elementom
6. Potrdimo z **OK**
7. Shranimo spremembe |mActionSaveAllEdits|

Orodje atributiranja
---------------------

Orodje vtičnika za atributiranje elementov omogoča paketno atributiranje elementov v enem koraku prilagojeno za izdelavo GJI elaborata.
Podrobnosti: :ref:`atributiranje`.

.. |mActionToggleEditing| image:: /_static/common/mActionToggleEditing.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionCaptureLine| image:: /_static/common/mActionCaptureLine.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionCapturePoint| image:: /_static/common/mActionCapturePoint.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionCapturePolygon| image:: /_static/common/mActionCapturePolygon.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionSaveAllEdits| image:: /_static/common/mActionSaveAllEdits.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mIconSnapping| image:: /_static/common/mIconSnapping.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionSplitFeatures| image:: /_static/common/mActionSplitFeatures.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionMergeFeatures| image:: /_static/common/mActionMergeFeatures.svg
   :width: 1.2em
   :class: no-scaled-link

.. |mActionMultiEdit| image:: /_static/common/mActionMultiEdit.svg
   :width: 1.2em
   :class: no-scaled-link