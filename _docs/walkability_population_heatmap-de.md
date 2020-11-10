---
title: Walkability Population Heatmap
permalink: de/docs/walkability population heatmap/
lang: de
---

Zusätzlich zu der [Walkability Heatmap](https://www.open-accessibility.org/docs/heatmap/), GOAT ermöglicht die Visualisierung eine weitere Heatmap, die als Walkability-Bevölkerungs-Index genannt ist. Diese Heatmap ermöglicht ein besseres Verständnis der Erreichbarkeit in einem bestimmten Gebiet oder in einer bestimmten Nachbarschaft mit Berücksichtigung der Bevölkerungszahl. Die Heatmap kann zur Beantwortung vieler Planungsfragen verwendet werden. Als Beispiel kann genannt werden:
- Wo kann in der untersuchten Nachbarschaft ein Erreichbarkeitssüberschuss gefunden werden?
- Wo kann in der untersuchten Nachbarschaft ein Dichteüberschuss gefunden werden?
- Wo ist eine Verdichtung erforderlich? 
- Wo ist eine Verbesserung der Erreichbarkeit zu bestimmten Einrichtungen oder ÖV Haltestellen notwendig?

{% include image.html src="docs/technical_documentation/walkability_population_index/walkability_population_map.png" %}

#### 1. Berechnung
Der Layer Walkability-Bevölkerungs-Index ergibt sich aus der Schnittmenge der beiden Layers Walkability und Bevölkerung.
{% include image.html src="docs/technical_documentation/walkability_population_index/intersection_2_layers.png" %}

#### 2. Klassifizierung
Um die Erreichbarkeitsstufen zu klassifizieren, die für jede Gitterzelle berechnet wurden, wird eine Klassifizierung basierend auf Perzentilen verwendet. Die folgende Tabelle zeigt, wie die Perzentile der Erreichbarkeit und der Bevölkerung in jedem Raster berechnet werden.

{% include image.html src="docs/technical_documentation/walkability_population_index/percentile.png" %}

Walkability-Bevölkerungs-Index wird wie folgt berechnet:

<b> Walkability Population Index = Population Level – Accessibility Level </b>

une zeigt folgendes Ergebnis:
{% include image.html src="docs/technical_documentation/walkability_population_index/calculated_index.png" maxheight="150px" %}


