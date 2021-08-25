---
title: Data Preparation
permalink: /de/docs/data_preparation/
lang: de
---


#### Data
There is one folder, `your-GOAT-directory/app/database/data`, in which you can organize the data you want to load into the database. 
The setup script will search for shapefiles (.shp), and SQL-table (.sql) dumps in this directory. All of the data will be uploaded as custom data tables into your database. In the following table, schemas for the most important custom datasets are described:  

##### Study Area
Table name: study_area
{% include image.html src="docs/technical_documentation/data_preparation/table_study_area.png" alt="Table schema study area" %}

##### Landuse
Table name: landuse
{% include image.html src="docs/technical_documentation/data_preparation/table_landuse.png" alt="Table schema land use" %}

##### Landuse additional
Table name: landuse_additional
{% include image.html src="docs/technical_documentation/data_preparation/table_landuse_additional.png" alt="Table schema additiona land use" %}

##### Census 
Table name: census
{% include image.html src="docs/technical_documentation/data_preparation/table_census.png" alt="Table schema census" %}

##### Buildings custom
Table name: buildings_custom
{% include image.html src="docs/technical_documentation/data_preparation/table_buildings_custom.png" alt="Table schema custom buildings" %}

##### Custom Population point data
Table name: population
{% include image.html src="docs/technical_documentation/data_preparation/table_population.png" alt="Table schema custom population data" %}

All attributes labelled as "not null" are required attributes. The remaining attributes are option but are suggested if available as they will improve the results. The described custom tables are especially used for the provision of population data. It is important to keep the described naming convention as GOAT expects the attributes to be labeled as shown. Not all tables are required to run GOAT and depending on the availability of data one or the other option to process population data is used. 

#### Population disaggregation

Accurate population data is of special importance for GOAT. Due to the variety of available data sets different options for handling population data are provided. There are defined four options for which the configuration file `your-GOAT-directory/app/config/goat_config.yaml` can be adjusted:

##### Options
<b>Census Standard</b>
Data originating from a census grid is disaggregated proportionally on the building access level considering the residential gross floor area of buildings. 

In goat_config.yaml: `POPULATION: "census_standard"`

Required tables: `study_area`, `census`

Optional tables: `landuse`, `landuse_additional`, `buildings_custom`

<b>Census Extrapolation</b>
As census data is often out of data a procedure was developed that updates outdates census grids and disaggregates population on the building access level. 

In goat_config.yaml: `POPULATION: "census_extrapolation"`

Required tables: `study_area`, `census`

Optional tables: `landuse`, `landuse_additional`, `buildings_custom`


<b>Population disaggregation</b>
Population is disaggregated from the districts of the study area to the building access level considering the residential gross floor area of buildings.

In goat_config.yaml: `POPULATION: "disaggregation"`

Required tables: `study_area`

Optional tables: `landuse`, `landuse_additional`, `buildings_custom`

<b>Custom population point data </b>
If custom population data sets is provided not disaggregation is performed. 

In goat_config.yaml: `POPULATION: "custom_population"`

Required tables: `population`

##### Classification buildings
For the modes "census_standard", "census_extrapolation" and "disaggregation" buildings are classified into residential and non-residential. This is done based on a process called dasymetric mapping, which uses several filters and data such as landuse to properly label buildings. 
In the configuration file `goat_config.yaml` these filters can be adjusted. The default settings are mostly tailored to Munich therefore it is highly suggested to revise categorization if you work in another context.

- <b>custom_landuse_no_residents</b>: if you have the table "landuse" you can define landuse categories that are not residential
- <b>custom_landuse_additional_no_residents</b>: if you have the table "landuse_addition" you can define landuse categories that are not residential
- <b>osm_landuse_no_residents</b>: landuse categories from OSM that you label as not residential (Check: [https://wiki.openstreetmap.org/wiki/landuse](https://wiki.openstreetmap.org/wiki/landuse))
- <b>building_types_potentially_residential</b>: building type that should not be excluded – <font color="red">Note: many buildings are just labeled building=yes in OSM</font>
- <b>building_types_residential</b>: building type that is for sure residential e.g. building=residential. This applied also to custom building data but mostly the OSM convention on building types is followed: [https://wiki.openstreetmap.org/wiki/Key:building](https://wiki.openstreetmap.org/wiki/Key:building))
- <b>tourism_no_residents</b>: <i>osm-tag tourism</i> that has no residents (Check: [https://wiki.openstreetmap.org/wiki/Tourism](https://wiki.openstreetmap.org/wiki/Tourism) )
- <b>amenity_no_residents</b>: <i>osm-tag amenity</i> that has no residents (Check: [https://wiki.openstreetmap.org/wiki/Key:amenity](https://wiki.openstreetmap.org/wiki/Key:amenity))
- <b>minimum_building_size_residential</b>: all buildings that have a smaller size than this are labeled as not residential (very often garages etc.)
- <b>average_gross_living_area</b>: the average gross living area in your study area per resident in m²
- <b>average_building_levels</b>: this is a fallback value in case no building levels are defined on the level of buildings or districts. 
- <b>average_roof_levels</b>: this is a fallback value in case no roof levels are defined on the level of buildings or districts. 
- <b>average_height_per_level</b>: this value is used to compute the number of building levels in case the height of buildings is know. 

