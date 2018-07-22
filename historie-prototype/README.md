Het komt voor dat bronsystemen geen mutatiehistorie bijhouden, terwijl dit wel wenselijk is. Dit prototype is ontwikkeld om mutatiehistorie op te bouwen in een feature class in de Enterprise Geodatabase. Het prototype gaat ervan uit dat de bron eveneens een feature class is, maar dat zal in werkelijkheid waarschijnlijk niet zo zijn. De workspace is daar echter eenvoudig op aan te passen.

In de historie wordt nooit een feature verwijderd. Verwijderde features worden afgesloten. Ze krijgen een `DATUM_VERVALLEN`. Van gewijzigde features wordt de oude versie afgesloten en een nieuwe aangemaakt.

Het prototype gaat ervan uit dat iedere feature in het bronsysteem een uniek `ENTITEIT_ID` heeft.

Een feature heeft in de historie drie extra attributen ten opzichte van het bronsysteem:
* `MUTATIE_ID`
* `DATUM_AANGEMAAKT`
* `DATUM_VERVALLEN`

De workspace is gemaakt in FME Desktop 2016 en getest met ArcGIS 10.3.1.

Voor demonstratie- en testdoeleinden zijn twee ESRI Workspace documenten toegevoegd. Hiermee kunnen de feature classes geïmporterd worden die nodig zijn om de FME workspace uit te voeren.