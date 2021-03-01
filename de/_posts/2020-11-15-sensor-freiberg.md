---
title:  "Test innovativer Ansätze zur Datenerfassung "
author: [ramirez, jehle, pajares]
lang: de
tags: [de]
categories: [news]
thumbnail: blog/sensor_freiberg/plots.png
image: blog/sensor_freiberg/plots.png
excerpt: Was verbindet GOAT mit einem Projekt für Lieferroboter? Die Nutzung derselben Infrastruktur!
Wir haben eine prototypische Sensorbox eingesetzt, um die automatisierte Erhebung von Straßendaten zu erproben. 
---
Stellen Sie sich einmal vor, Sie öffnen die Tür, um Ihre Essens- oder Amazon-Lieferung in Empfang zu nehmen und… Überraschung! Vor Ihnen steht der kleine Roboter Wall-E aus dem gleichnamigen Disney-Film! Wie bitte? Wall-E? Naja, nicht ganz. Aber eines Tages könnten tatsächlich Lieferungen von autonomen Robotern durchgeführt werden. Moment… waren autonome Fahrzeuge nicht etwas, das Autos, Zügen oder LKWs vorbehalten war? Ganz und gar nicht! Autonome Fahrzeuge gibt es in den unterschiedlichsten Größen. Doch wie jedes selbstfahrende Fahrzeug, stehen auch diese vor einer der größten Herausforderungen, um uneingeschränkt zu funktionieren: sie brauchen ein genaues Bild der Umgebung, in der sie sich bewegen. 
Aus diesem Grund arbeitet das Team von Prof. Sebastian Zug am [Lehrstuhl für Softwaretechnologie und Robotik an der TU Bergakademie Freiberg](https://tu-freiberg.de/fakult1/inf/professuren/softwaretechnologie-und-robotik) am [Projekt “AK hoch 2“](https://www.bmvi.de/SharedDocs/DE/Artikel/DG/mfund-projekte/akhoch2.html). Das Projekt wird vom Bundesministerium für Verkehr und digitale Infrastruktur gefördert, um die Qualität und die Eigenschaften der Fahrradinfrastruktur zu erfassen. Das konkrete Ziel dieses Projektes ist insbesondere, die Parameter von Radwegen und Fußgängerwegen systematisch zu aggregieren. Dazu wurde ein mobiles Messsystem entwickelt, welches an jedem Fahrrad befestigt werden kann. Es wertet Bewegungssensoren aus und kombiniert diese Informationen mit Informationen über den Standort. Schließlich identifiziert eine KI-basierte Klassifizierung die Art der Oberfläche und die Oberflächenglätte und lokalisiert so Hindernisse. 

{% include image.html src="blog/sensor_freiberg/sensors.png" maxheight="400px" %} 
<i>Abbildung 1. Die Sensorbox, entwickelt von der TU Bergakademie Freiberg</i>

Doch wie kommt die Verbindung zwischen GOAT und dem Projekt für Lieferroboter zustande? Natürlich, weil wir dieselben Geh- und Fahrradwege nutzen. Das Hauptziel des Projektes ist das Sammeln von Informationen über die Rad- und Gehweginfrastruktur, daher teilen wir ein sehr wichtiges, gemeinsames Interesse: zuverlässige und genaue räumliche Daten. Aus diesem Grund haben wir den Sensorbox-Prototypen für unsere Mapping-Aufgaben vor Ort genutzt, um Informationen zu sammeln. Hier folgt ein kleiner Einblick in unsere Aufnahmen.

{% include image.html src="blog/sensor_freiberg/cyclepath.png" maxheight="400px" %} 
<i>Abbildung 2. Exemplarische Fahrradroute, die mit dem Messgerät erfasst wurde. </i>

Das Gerät zeigt die befahrene Strecke an und der Anwendende muss jeweils die Kategorie der benutzten Infrastruktur (Straße, Fahrradweg oder Fußweg) angeben. Anschließend wird die GNSS-Position durch einen MapMatching-Algorithmus harmonisiert, der den daraus abgeleiteten Standort mit Informationen aus OpenStreetMap miteinander vergleicht. Aber der Sensor ist sehr viel mehr als einfach nur ein GNSS und ein Geschwindigkeitsmesser. 

{% include image.html src="blog/sensor_freiberg/plots.png" maxheight="400px"%} 
<i>Abbildung 3. Gemessene Beschleunigung in allen drei Dimensionen</i>

Der Sensor verfügt über einen Beschleunigungsmesser, der kontinuierlich Veränderungen in allen drei Achsen sowie ihre Vektorsumme misst. Aus den Beschleunigungsgrafen ist es möglich, bestimmte Verhaltensweisen als Beschleunigung und Bremsen anhand von Änderungen der X-Achse zu identifizieren, wo „unter null“ als bremsen gewertet werden kann und „über null“ als beschleunigen. Auf der Y-Achse ist es ebenfalls möglich, eine konstante Schwingung zu erkennen. Auf der Graphik erscheinen allerdings größere Ausschläge. Sie könnten in Zusammenhang mit Straßenunebenheiten oder einer rauen Straßenoberfläche stehen. Abschließend und bezogen auf die Z-Achse, ist es möglich, scharfe Veränderungen in der horizontalen Ausrichtung der Infrastruktur oder Hindernisse zu erkennen, die möglicherweise eine reibungslose Fahrt verhindert haben. 

Können Sie sich noch an [unsere Erfahrungen mit Mapillary in Fürstenfeldbruck](../mapillary) erinnern? Dieses Mal nutzen wir denselben Prozess, um sowohl die Erhebung von Beschleunigungsdaten als auch die Straßenbilder mit Intervallen von einer Sekunde zu haben, um ein besseres Verständnis der Straßenbedingungen zu erhalten. Die ersten Ergebnisse sind vielversprechend und wir freuen uns darauf, das Gerät in unserem Einsatz für bessere Kartendaten weiterhin zu nutzen.
