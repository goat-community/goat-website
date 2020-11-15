---
title: Szenarien - Wege
permalink: /de/tutorials/scenario-ways/
lang: de
---

#### Beschreibung des Features
GOAT ermöglicht die Entwicklung eigener Szenarien, wie z.B. Modifikation des Netzwerks oder Bau einer neuen Brücke. Das entwickelte Szenario kann zu dem aktuellen Netzwerk hinzugefügt und Änderungen der Erreichbarkeit durch Isochronen bewertet werden. 

#### Mögliche Anwendungsfälle (Planungsfragen)
- Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss?
- Wie verändert sich die Erreichbarkeit mit dem Rollstuhl durch den Bau einer barrierefreien Wegeverbindung? 
- Welche Variante eines neuen Radweges erschließt die höchste Anzahl an Anwohner?


#### Schritt-für-Schritt-Anleitung für eine beispielhafte Planungsaufgabe
##### 1 Szenario zu neuer Fahrradbrücke
###### 1.1 Planungsfrage
Wie verändert sich die Erreichbarkeit durch den Bau einer neuen Fahrradbrücke über einen Fluss? 
###### 1.2 Arbeitsschritte
1. Gehen Sie in das Fenster zur Szenarienentwicklung und erstellen Sie ein neues Szenario.  {% include image.html src="../../uploads/training materials/Scenario_POIs/create_scenario.png" maxheight="200px" %} 

2. Geben Sie dem Scenario einen Namen und klicken Sie auf "OK".  {% include image.html src="../../uploads/training materials/Scenario_building/name_scenario.png" maxheight="200px" %}

3. Wählen Sie welchen Layer Sie bearbeiten möchten, in diesem Fall den „Wege“ Layer.  {% include image.html src="../../uploads/training materials/Scenario_building/scenario_ways.png" maxheight="200px" %}


4. Zoomen Sie zu der Stelle, an der Sie eine neue Fahrradbrücke bauen wollen und wählen Sie mittels des Kreis-Werkzeuges das umliegenden Straßennetz aus.  {% include image.html src="../../uploads/training materials/Scenario_building/circle_scenario.png" %}

5. Zeichnen Sie an der gewünschten Stelle eine neue Wegeverbindung, wählen als Wegetyp „Brücke“ aus und klicken Sie auf „Speichern“. Die gezeichneten Wege werden nun rechts in der Tabelle aufgeführt. Um diese Wege in die Datenbank zu integrieren, müssen diese über den Button „Hochladen“ hochgeladen werden.  {% include image.html src="../../uploads/training materials/Scenario_building/bridge_building.png" maxheight="300px"%}

6. Nun können Sie die Auswirkung der neuen Wegeverbindung auf die Erreichbarkeit analysieren, indem Sie sich die Standard- und die Scenario-Isochrone berechnen lassen. Wählen Sie hierzu den Routingmodi „Fahrrad“ aus und setzen den Berechnungsmodus auf „Vergleich“. In den Optionen können Sie die Reisezeit, die Fahrgeschwindigkeit und die Anzahl der zuberechnenden Isochronen einstellen.  {% include image.html src="../../uploads/training materials/Scenario_building/comparison.png" maxheight="300px" %}

7. Platzieren Sie den Startpunkt für die Isochronenberechnung in der Nähe der neuen Brücke. Als Ergebnis wird Ihnen in Rot die Isochrone in der Ausgangslage und in Grün die Isochrone unter Berücksichtigung der neuen Wegeverbindung angezeigt.  {% include image.html src="../../uploads/training materials/Scenario_building/result-isochrone.png" %}

