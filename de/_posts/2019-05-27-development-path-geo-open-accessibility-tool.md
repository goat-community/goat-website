---
permalink: /de/development-path-geo-open-accessibility-tool/
title:  "Der Entwicklungspfad von GOAT"
author: [pajares]
lang: de
tags: [de]
thumbnail: blog/development_path/thumbnail.png
image: blog/development_path/thumbnail.png
---

Das Geo Open Accessibility Tool (GOAT) ist aktuell noch nicht dort, wo wir einmal hin möchten. Neben der fortwährenden Professionalisierung, die unabdingbar für ein wirklich nützliches und stabiles Erreichbarkeitsinstrument ist, werden in regelmäßigen Abständen weitere Funktionen implementiert.  

Das Hauptanliegen, worauf wir uns in den vergangenen Monaten konzentriert haben, war es, die interaktive Netzwerkmodifikation und den Set-up Prozess zu verbessern. Dabei wurde bisher wenig Zeit investiert, um neue Features zu implementieren. Dennoch gibt es einige neue, innovative Funktionen, die bereits angedacht sind. Diese werden GOAT zu dem Status verhelfen, in dem die erste Version (GOAT 1.0) veröffentlicht wird. 

GOAT ist bislang in jeder Hinsicht noch ein persönliches Projekt, da die Finanzierung für die erste Veröffentlichung noch nicht gesichert ist. Folglich bleibt noch undefiniert, wann dieser bahnbrechende Release 1.0 stattfinden und GOAT somit vermarktet werden kann. Wir schätzen, dass dies in ein bis zwei Jahren umgesetzt wird. Ich finde es dennoch wichtig, die potenziellen künftigen Funktionen von GOAT zu kommunizieren und aufzuzeigen, welche Wege dieses Instrument einschlagen wird. Einige GOAT-Funktionen werden im Laufe der Entwicklung hinzukommen, während andere womöglich entfernt werden. 

Die folgende Tabelle gewährt einen Einblick in die Entwicklungsfelder. Dabei muss betont werden, dass sie nicht vollständig ist und vor allem kleinere Funktionen sowie Funktionen, die das Nutzererlebnis betreffen, nicht aufgeführt sind.

<table class="table table-striped table-hover ">
  <thead>
    <tr>
      <th>Funktion</th>
      <th>Beschreibung</th>
      <th>Offene Aufgaben</th>
    </tr>
  </thead>
  <tbody>
    <tr class="success">
      <td><b>Routing-Performance</b></td>
      <td>Die pgRouting Bibliothek glänzt mit ihrer Flexibilität, wobei dies mit einer relativ langen Abfragezeit des kürzesten Weges und der Isochronen einher geht. Neue Funktionen wie Multi-Isochronen sind aber auf effizientere Kalkulationen angewiesen. Obwohl pgRouting nicht standardmäßig auf High-Performance eingestellt ist, kann die Performance gesteigert werden: durch eine gute Netzwerkvorbereitung sowie verbesserte SQL-Abfrage. Es wird ebenfalls geprüft, ob Datenbank-Cluster oder die Berechnung auf unterschiedlichen Prozessorkernen die Performance steigern kann.</td>
      <td>Die Arbeit zur Steigerung der Performance hat bereits begonnen. Allerdings wird es mit dem neuen Modus für Radfahrer und der Implementierung von neuen Zugänglichkeitsindikatoren eine fortwährende Challenge bleiben.</td>
    </tr>
    <tr class="success">
      <td><b>Berechnung von Multi-Isochronen</b></td>
      <td>Der Nutzer hat zurzeit lediglich die Möglichkeit, eine einzige Isochrone zu berechnen, indem er auf die Karte klickt. Eine neue Funktion soll die gleichzeitige Berechnung von unterschiedlichen Ausgangspunkten aus ermöglichen. Als Startpunkt können bestimmte Einrichtungen ausgewählt und die Isochronen alle gleichzeitig dargestellt werden. Das könnte bestimmte Fragen beantworten, wie: wie hoch ist der Anteil der Anwohner, die innerhalb von 10 Gehminuten eine Schule erreichen können?</td>
      <td>Diese neue Funktion geht Hand in Hand mit der anvisierten Leistungssteigerung der pgRouting-Funktionen. Die SQL-Funktionalität ist ebenfalls zum Teil bereits beendet. Lediglich die Implementierung in das Front-End hat noch nicht begonnen.</td>
    </tr>
    <tr class="success">
      <td><b>Modifikation von POIs</b></td>
      <td>Diese Funktion kann als erster Schritt angesehen werden, der es Nutzern erlaubt, die Auswirkungen von Flächennutzungsänderungen zu modellieren. Diese experimentelle Funktion soll es Nutzern ermöglichen, POIs zu zeichnen, zu modifizieren oder zu löschen. Durch die interaktive Netzwerkveränderung kann der Nutzer Erreichbarkeitsanalysen durchführen und dabei die Flächennutzungsänderungen einfließen lassen. Als interessantes Szenario könnten u.a. folgendes analysiert werden: Wie verändert sich die fußläufige Erreichbarkeit bei einer besseren räumlichen Verteilung der Einrichtungen?</td>
      <td>Momentan ist nur wenig Interaktion mit den POIs möglich. Daher müssen zunächst einige Funktionen (bspw. das Clustern von Zielen) implementiert werden, die eine interaktivere und visuell ansprechendere Art der Interaktion mit den Zielen erlauben.</td>
    </tr>
    <tr class="warning">
      <td><b>Individuelle Routing-Profile</b></td>
      <td>ie Verbesserung der Modellierung der individuellen Erreichbarkeitskomponente ist eines der Hauptziele von GOAT. Hier besteht die Notwendigkeit, die Routen-Funktionalität individuell anzupassen, um die Schwierigkeiten, die mobilitätseingeschränkte Menschen täglich haben, besser abzubilden und somit die  Barrierefreiheit einzubeziehen. Zusätzlich soll die Routing-Funktionalität dahingehend verfeinert werden, Zeitverlust bei Kreuzungen, Steigungen oder andere Barrieren abzubilden.</td>
      <td>Für die theoretische Seite ist bereits eine signifikante Vorarbeit geleistet worden (bspw. im Rahmen einer exzellenten Bachelorarbeit an der TUM). Wobei noch weitere empirische Erkenntnisse zur Beeinflussung der Gehgeschwindigkeit unterschiedlicher Personengruppen erlangt werden müssen, besonders in Bezug auf die Beeinflussung durch Barrieren.</td>
    </tr>
    <tr class="warning">
      <td><b>Neuer Routing-Modus: Radverkehr</b></td>
      <td>Die Modellierung für den Fahrradverkehr ist eine der an den häufigsten gewünschten Funktionen. Die Herausforderung hierbei ist es, eine realistische Routing-Funktionalität zu haben. Das Ziel ist es, Radfahren für unterschiedliche Nutzergruppen und Bedingungen abzubilden. Die Vorarbeit dazu wurde bereits im Rahmen eines sehr guten Studienprojekts an der TUM geleistet. Dessen Ergebnisse werden weiter verfeinert und in die Gesamtarchitektur integriert.  </td>
      <td>Ein Teil der Backend-Funktionalität ist bereits vollendet, aber das Frontend und vor allem die Integration in die interaktive Netzwerk-Modifikationsfunktionalität erfordert noch weitere signifikante Ressourcen. Dennoch wird eine experimentelle Version dieser Funktion bald veröffentlicht werden.</td>
    </tr>
    <tr class="danger">
      <td><b>Dynamische Neuberechnung der Heatmap</b></td>
      <td>Die verwendete Heatmap basiert auf vorberechneten Reisezeiten. Das ist super für die Performance, geht allerdings auf Kosten der Berechnung, die nicht dynamisch ist. Mit der gegebenen Architektur und den vorhandenen Ressourcen ist eine dynamische Neuberechnung nicht in einer annehmbaren Rechenzeit möglich. Es müssen Wege gefunden werden, auch eine dynamische Neuberechnung für diesen Indikator zu ermöglichen.</td>
      <td>Für diese Funktion wird eine signifikante Leistungssteigerung der Routing-Funktionen vorausgesetzt. Nachdem das erreicht wurde, muss die Heatmap-Funktionalität weiter verfeinert und dahingehend angepasst werden, dass die Abbildung von Szenarien ermöglicht werden.</td>
    </tr>
    <tr class="danger">
      <td><b>Komplette Flächennutzungsänderung </b></td>
      <td>Ziel dieser Funktion ist es, den Nutzern die Möglichkeit zu geben, die Flächennutzungsdaten komplett verändern zu können. Der Nutzer soll nicht nur neue POIs hinzufügen können, sondern in der Lage sein, eigene Gebäudedaten hochzuladen, Einwohner und Jobs zuzuordnen und vieles mehr. Diese Funktion wird als ein essenzieller Teil betrachtet, um GOAT als Werkzeug zur Entwicklung von Stadtentwicklungsplänen zu verwenden.</td>
      <td>Diese Funktion benötigt einen erheblichen Aufwand, sowohl im Frontend als auch im Backend, da dort umfangreiche Entwicklungen durchgeführt werden müssen. Die Voraussetzung für dieses Feature ist außerdem eine sehr hohe Benutzerfreundlichkeit.</td>
    </tr>

  </tbody>
</table>

Ich bin sehr offen für weitere Ideen oder Vorschläge aus der Community. GOAT ist ein Open-Source-Projekt und zielt daher auf eine starke Interaktion mit den Nutzern ab. Gerne einfach Kontakt aufnehmen! 

Zusätzlich zu den aufgelisteten Verbesserungen, ist ein Schwerpunkt auch auf Datenfusionskonzepte und ein stärkeres Engagement in der OpenStreetMap-Community (OSM) ausgerichtet. Diejenigen, die GOAT bereits getestet haben, haben eventuell bereits bemerkt, dass die Demo-App momentan nur für die Stadt München erhältlich ist. GOAT kann zwar von jedem auf seinem eigenen Server installiert werden, viele wünschen sich aber, GOAT sofort in ihrem Anwendungsbereich nutzen zu können. 

Der Grund, weshalb noch nicht weitere Orte abgedeckt werden, sind die hohen Anforderungen an Datenqualität und Ressourcen, die ich für zusätzlichen Serverplatz bräuchte. OSM-Daten können in ihrer Qualität variieren, daher ist es aus meiner Sicht unabdingbar Gegenkontrollen mit lokalem Wissen sowie anderen Datenquellen durchzuführen. Vor allem, wenn die Daten zu im realen Planungsbetrieb verwendet werden.  

Bis zu diesem Tag bin ich bisher ausschließlich in der Lage, GOAT für die Stadt München anzubieten. Ich kann mir aber vorstellen, die Online-Version von GOAT für weitere Kreise in der Metropolregion München auszuweiten.  

Ich bin auch sehr offen dafür, GOAT in anderen Städten weltweit als Initiative zur Förderung von bedeutsamer Zusammenarbeit mit anderen zu etablieren. Wenn Sie GOAT in Ihrer Stadt vermissen und daran interessiert sind, Teil der Community zu werden, kontaktieren Sie mich einfach und ich werden Strategien entwickeln, um dies zu ermöglichen.  
