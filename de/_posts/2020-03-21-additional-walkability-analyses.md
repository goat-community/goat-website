---
permalink: /de/additional-walkability-analyses/
title:  "Zusätzliche Analysen zur Walkability"
author: [jehle]
lang: de
tags: [de]
categories: [news]
thumbnail: blog/additional_walkability_analyses/scenery_hasenbergl.jpg
image: blog/additional_walkability_analyses/scenery_hasenbergl.jpg
excerpt: Um lebenswerte Städte zu gestalten und eine nachhaltigere Mobilität zu prägen, ist es unabdingbar sich auf fußläufig erreichbare Umgebungen zu konzentrieren. Die wahrgenommene Qualität der Infrastruktur ist allerdings stark vom Einzelnen abhängig. In Deutschland sind zum Beispiel ein Drittel der Bevölkerung temporär Mobilitätseingeschränkt und 28% der Bevölkerung ist über 60 Jahre alt. Dies führt zu individuellen Bedürfnissen, wie beispielsweise ebene Bodenoberflächen und barrierefreie Gehwege.
---


<i> 
- Dieser Blogpost stellt eine Zusammenfassung meiner Masterarbeit dar. Bei Interesse an weiteren Details kann das komplette Dokument unten heruntergeladen werden. - 
</i>


Um lebenswerte Städte zu gestalten und eine nachhaltigere Mobilität zu prägen, ist es unabdingbar sich auf fußläufig erreichbare Umgebungen zu konzentrieren. Die wahrgenommene Qualität der Infrastruktur ist allerdings stark vom Einzelnen abhängig. In Deutschland sind zum Beispiel ein Drittel der Bevölkerung temporär Mobilitätseingeschränkt und 28% der Bevölkerung ist über 60 Jahre alt. Dies führt zu individuellen Bedürfnissen, wie beispielsweise ebene Bodenoberflächen und barrierefreie Gehwege. Um eine gute fußläufige Erreichbarkeit zu gewährleisten müssen all diese individuellen Bedürfnisse im Planungsprozess einbezogen werden. Das macht die Bereitstellung einer geeigneten Infrastruktur zu einer recht komplexen Herausforderung.

Zugänglichkeitsinstrumente können als Planungshilfen dienen und dabei helfen diese Herausforderungen anzugehen. Idealerweise werden alle vier Komponenten der Erreichbarkeit (Flächennutzungskomponente, Transportkomponente, Zeitkomponente, individuelle Komponente) in einem einzigen Erreichbarkeitsinstrument dargestellt. Diese Arbeit untersucht wie diese vier Komponenten in GOAT einbezogen werden können. Um das zu realisieren, wurde das Schema der vier Erreichbarkeitskomponenten mit den zugehörigen Attributen wie im folgenden Schaubild dargestellt, in GOAT angewandt.

{% include image.html src="blog/additional_walkability_analyses/four_accessibility_components.png" alt="Das Schema der vier Erreichbarkeitskomponenten, übertragen auf GOAT" %}
(adaptiert von Geurs und van Wee 2004)

Als Untersuchungsbereich wurde “Hasenbergl-Lerchenau”, eines der Stadteile mit dem niedrigsten Durchschnittseinkommen Münchens, mit einer Größe von 869ha und einer Population von 46.953, ausgewählt. Alle notwendigen Daten wurden in OpenStreetMap (OSM) mittels der iOS App “Go Map!!”, JOSM und Mapillary erfasst. Obwohl die OSM-Daten im Untersuchungsbereich überwiegend geometrisch korrekt waren und Objekte wie das Straßennetzwerk und die Gebäude beinahe vollständig abgebildet waren, fehlten wesentliche Attribute für diese Studie. Beispielsweise gab es nur bei 5% aller Wege Informationen über die Beleuchtung und bei nur 3% der Wege über gab es Informationen über die Gehwegverfügbarkeit. In 20 Tagen Datenerhebung vor Ort und anschließender Datenaufbereitung, wurden alle 2.000 vorhandenen Wege mit einer Gesamtlänge von über 200km in OSM erfasst. Einschließlich Informationen über die Straßenart, Belag, Steigung, Gehwegverfügbarkeit, Wegebreite, Beleuchtung und Barrierefreiheit. Genauso wurde die Zugänglichkeit für Rollstuhlfahrer für alle POIs erfasst. Dadurch konnte die Datenqualität insgesamt stark verbessert werden (Siehe Kapitel 6.3. der Arbeit).

{% include image.html src="blog/additional_walkability_analyses/scenery_hasenbergl.jpg" alt="Aufnahme aus dem Studiengebiet (Hasenbergl)" %}

Mit den verbesserten Daten konnten neue Features in GOAT implementiert werden. Um die individuelle und die zeitliche Komponente zu repräsentieren, wurden drei neue Routing-Profile (Senior, Rollstuhl, sicheres Nacht-Routing) hinzugefügt, die einen Einfluss auf die Wahl der Route und auf die Gehgeschwindigkeit haben. Die Rollstuhl-Option berücksichtigt nur barrierefreie Wege und Zielorte, während das sicheres Nacht-Routing nur Wege wählt, die nachts beleuchtet sind. Auch die Öffnungszeiten von POIs wurden in die Berechnungen einbezogen, um eine zeitbasierte Erreichbarkeits-Analyse zu ermöglichen (detaillierte Informationen dazu gibt es in Kapitel 7). 

Die Analyse der ermittelten Daten offenbart, dass es im Untersuchungsgebiet eine hohe Anzahl von unbeleuchteten und nicht-barrierefreien Wegen gibt, die als wichtige Fußwege-Verbindungen gelten. Die folgende Abbildung zeigt einen Erreichbarkeits-Vergleich zwischen dem Standard und dem sicheren Nacht-Routing von einem Startpunkt innerhalb eines Wohngebietes unter Verwendung einer 7-Minuten-Gehischochrone. Die Verkleinerung der Isochrone zeigt auf, dass die Erreichbarkeit, unter Berücksichtigung dieser (tages)zeitlichen Komponente, deutlich reduziert wird.

{% include image.html src="blog/additional_walkability_analyses/comparison_walking_accessibility.png" alt="Vergleich der fußläufigen Erreichbarkeit Tag - Nacht" %}

Ähnliche Ergebnisse erhält man auch bei der barrierefreien Routingoption. Außerdem wurde festgestellt, dass viele POIs nicht für Menschen mit Mobilitätseinschränkungen zugänglich sind. Meistens liegt dies daran, dass sich Stufen am Eingang befinden. Durch die Berechnung der Multi-Isochronen, kann die Rollstuhl-Erreichbarkeit wichtiger Einrichtungen, wie beispielsweise von Ärztehäusern, berechnet werden. Das folgende Video zeigt alle Ärzte, die innerhalb eines 10-Gehminuten-Einzugsbereich liegen, wenn die Standart-Routingoption ausgewählt wird und die selbe Analyse, bei Auswahl des Rollstuhl-Profils, im Vergleich. Daraus ergibt sich, dass ca. 8.880 Menschen von einer Gesamtbevölkerung von 46.950 keinen barrierefreien Zugang zu Ärzten innerhalb eines 10-minütigen Fußwegs haben. Weitere Analysen finden sich im Kapitel 9 der Masterarbeit. 

<iframe class="embed-responsive-item" src="https://player.vimeo.com/video/399481443" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen data-uk-responsive width="1920" height="1080"></iframe>


Außerdem wurde das Frontend angepasst, um weitere Layer zu verschiedenen Kriterien zur fußläufigen Erreichbarkeit zu visualisieren (Beleuchtung, Rollstuhltauglichkeit, Gehwegbreite, Oberflächenbeschaffenheit, Anzahl der Fahrspuren, Höchstgeschwindigkeit, Parkmöglichkeiten, Straßenkreuzungen, Stadtmöbel), wodurch die Transportkomponente realistischer dargestellt wird (Kapitel 8). Diese Layer liefern den Anwender*Innen nützliche Informationen, und ermöglichen dadurch Schwachstellen im Fußwegnetzwerk leicht zu erkennen. 
Die objektiv erhobenen Qualitätskriterien der Straßenebene können jedoch nicht das gesamte Konzept der fußläufigen Erreichbarkeit abdecken, daher wurden auch Aussagen von Passanten über die wahrgenommene Qualität der fußläufigen Erreichbarkeit einbezogen, um so ein umfassenderes Bild zu liefern. Das stellte sich als besonders wertvoll heraus, da die wahrgenommene Qualität oft von der objektiv gemessenen Qualität abweicht.


Mit den implementierten Änderungen konnten alle vier Erreichbarkeits-Komponenten in GOAT integriert werden. Diese Ergänzungen bieten spannende Einblicke, wie die fußläufige Erreichbarkeit von unterschiedlichen Nutzergruppen durch Änderungen der zeitlichen und individuellen Komponente beeinflusst wird. So wurde GOAT erweitert, um eine ganzheitlichere Erreichbarkeitsanalyse zu ermöglichen. Da diese Analyseoptionen stark von der Datenverfügbarkeit abhängen, sind nicht alle neuen Funktionen standardmäßig in GOAT integriert. Die Funktionen können aber je nach lokalem Kontext aktiviert oder deaktiviert werden.

Diese Implementierung kann als erster Versuch zur besseren Modellierung der zeitlichen und individuellen Komponente der fußläufigen Erreichbarkeit angesehen werden. Weitere Ergänzungen und Verbesserungen werden in Zukunft folgen. Wir sind sehr offen für Feedback und freuen uns auf Ihre Anregungen!


Die GOAT-Version von Hasenbergl-Lerchenau enthält alle neuen Funktionen und kann [hier](https://hasenbergl.open-accessibility.org/) getestet werden. 


Die komplette Masterarbeit kann [hier](https://mediatum.ub.tum.de/604993?query=Ulrike+Jehle&show_id=1542813)runtergeladen werden.