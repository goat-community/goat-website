---
title: Walkability Population Heatmap
permalink: de/docs/walkability population heatmap/
lang: de
---

Zusätzlich zur [Walkability Heatmap](https://www.open-accessibility.org/docs/heatmap/) ermöglicht GOAT die Visualisierung einer weiteren Heatmap, genannt Walkability-Bevölkerungs-Index. Diese Heatmap ermöglicht ein besseres Verständnis der Erreichbarkeit in einem bestimmten Gebiet oder in einer bestimmten Nachbarschaft unter Berücksichtigung der Bevölkerungsdichten. Die Heatmap kann zur Beantwortung vieler Planungsfragen verwendet werden, wie zum Beispiel:
- Wo herrscht in der untersuchten Nachbarschaft ein Erreichbarkeitssüberschuss?
- Wo herrscht in der untersuchten Nachbarschaft ein Dichteüberschuss?
- Wo ist Potenzial für (Nach-)Verdichtung? 
- Wo ist eine Verbesserung der Erreichbarkeit zu bestimmten Einrichtungen oder ÖV Haltestellen notwendig?

{% include image.html src="docs/technical_documentation/walkability_population_index/walkability_population_map.png" %}

#### 1. Berechnung
Die Walkability-Bevölkerung-Heatmap ergibt sich aus der Schnittmenge der beiden Layer Walkability und Bevölkerung.
{% include image.html src="docs/technical_documentation/walkability_population_index/intersection_2_layers.png" %}

#### 2. Klassifizierung
Zur Klassifizierung der Erreichbarkeitswerte, die für jedes Hexagon berechnet wurden, wird eine Einteilung basierend auf Perzentilen verwendet. Die folgende Tabelle zeigt examplarisch, wie sich die Erreichbarkeitswerte zusammensetzen.
{% include image.html src="docs/technical_documentation/walkability_population_index/percentile.png" %}

Der Walkability-Bevölkerungs-Index wird wie folgt berechnet:

<b> Walkability Population Index = Population Level – Accessibility Level </b>

und zeigt folgendes Ergebnis:
{% include image.html src="docs/technical_documentation/walkability_population_index/calculated_index.png" maxheight="150px" %}


