---
title: Mapping Mode
permalink: /de/docs/mapping_mode/
lang: de
---
Welcome and thank you for your interest in contributing to the quality of open data. With this feature, we are organizing and setting the mapping tasks that are necessary to improve some of the OSM data used by the GOAT tool. The focus is on rather simple mapping tasks, such as adding attributes. This feature is available in our GOAT versions for Munich, Fürstenfeldbruck and Freising. For Freising and Fürstenfeldbruck we created as well some [MapRoulette challenges](https://maproulette.org/browse/challenges/13812) where you are highly welcome to contribute.

In the following, you will find the steps to use GOAT’s editing tool “OSM Mapping Mode”.

#### 1. Open GOAT OSM Mapping Mode
First choose the desired GOAT location [here](https://www.open-accessibility.org/versions).
In the tool, you will notice the OSM logo in the right-bottom corner.

{% include image.html src="docs/mapping_mode/mapping_mode.png" alt="Activate the OSM Mapping Mode" title="OSM Mapping Mode" %}

By clicking here, you will see our Welcome message to the OSM Map Mode, and the left banner with the Isochrones and Layers menu is replaced by the OSM Mapping Tasks.

#### 2. Select one of the tasks

Now, on the OSM Mapping Tasks menu you will see our tasks available (highlighted in the next image). Each of these topics filters and shows you the objects in the map that still have missing information which is important to improve the performance of GOAT.

{% include image.html src="docs/mapping_mode/mapping_tasks.png" alt="The left menu shows the available mapping tasks" title="Available Mapping Tasks" %}

#### 3.	What to do?

We have set up different tasks for objects with missing information, which can be completed using the iD-Editor or other OSM editors such as JOSM. This list of tasks will be frequently updated. Remember always to follow the standards and characteristics established in the OSM-Wiki for each task as this data will be updated for all OSM users. 
<table class="table table-striped table-hover">
  <thead>
    <tr>
      <th style="width:100px">Tasks</th>
      <th style="width:250px"> Missing Information</th>
      <th style="width:170px">Possible Sources</th>
      <th style="width:80px">OSM Wiki</th>
    </tr>
  </thead>
  <tbody>
    <tr class="success">
      <td><b>Buildings – Building Type</b></td>
      <td>Value for the building type (e.g. apartments, commercial, church, public)</td>
      <td>•	Mapillary Street View <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:building">https://wiki.openstreetmap.org/wiki/Key:building</a></td>
    </tr>
    <tr class="success">
      <td><b>Ways – Surface Type</b></td>
      <td>Value of the surface (e.g. paved, asphalt, paving stones, compacted)</td>
      <td>•	Aerial images or photos <br>
          • Mapillary Street View <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:surface">https://wiki.openstreetmap.org/wiki/Key:surface</a></td>
    </tr>
    <tr class="success">
      <td><b>Ways – Cycleway Segregated</b></td>
      <td>Segregation between cycleway and footpath (e.g. yes, no)</td>
      <td>• Mapillary Street View <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:segregated">https://wiki.openstreetmap.org/wiki/Key:segregated</a></td>
    </tr>
    <tr class="success">
      <td><b>Ways – Cycleway Width</b></td>
      <td>Width of the cycleway in meters (e.g. 1.0, 1.5, 2.0)</td>
      <td>• Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:width">https://wiki.openstreetmap.org/wiki/Key:width</a></td>
    </tr>
    <tr class="success">
      <td><b>Ways – Parking Lanes</b></td>
      <td>Value of the parking lane (e.g. parallel, diagonal, perpendicular, no_parking)</td>
      <td>•	Aerial images or photos <br>
          • Mapillary Street View <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:parking:lane">https://wiki.openstreetmap.org/wiki/Key:parking:lane</a></td>
    </tr>
    <tr class="success">
      <td><b>Ways – Maxspeed</b></td>
      <td>Maximum Speed Limit (e.g. 30, 50, 100)</td>
      <td>•	Mapillary Street View <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Speed_limits">https://wiki.openstreetmap.org/wiki/Speed_limits</a></td>
    </tr>
    <tr class="warning">
      <td><b>POIs – Opening Hours</b></td>
      <td>Values of opening hours (take into account weekends, holidays, multiple days, e.g. Mo-Th 08:00-20:00; Fr-Su 10:00-20:00)</td>
      <td>•	Website of the amenity <br>
          • Personal Site Visit</td>
      <td><a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td>
    </tr>
  </tbody>
</table>

If you have questions on how to edit objects in OSM you can visit our page [Making changes in OSM](../osm_tutorial/) for further information. In case you are still not sure how to map a dedicated feature it is better to just leave the task open. 

#### 4.	How to edit?

Once you select the task you want to work on, the map will show the objects that have missing information about the selected feature (e.g. building type).

{% include image.html src="docs/mapping_mode/building_types.png" alt="All buildings with missing information are displayed" title="Mapping task on missing building types" %}

Now you can click one of the elements from the map, this will open a pop-up window showing the current information available. To edit the element and add additional information click on “Edit with OSM”. 

{% include image.html src="docs/mapping_mode/edit_building_types.png" alt="Edit one of the displayed buildings" title="Edit one of the displayed buildings" %}

This will redirect you to the OpenStreetMap website and will ask you to enter your username and password.

{% include image.html src="docs/mapping_mode/osm_login.png" alt="Log in into OSM" title="OSM Log In" %}

Once you have logged in, you will be in the iD-Editor from OpenStreetMap. This online tool allows you to add the new information for each of the objects and perform further edits as changing the shape of buildings and streets and even create new elements from scratch. For more information about iD Editor you can visit the [OSM Wiki](https://wiki.openstreetmap.org/wiki/ID).

{% include image.html src="docs/mapping_mode/osm_building_editing.png" alt="Add the missing information" title="Add the missing information" %}

To make use of Mapillary’s integrated tool within the iD Editor, click on the Map Data button from the menu on the right, and then turn on the option for Mapillary. The green tracks available for street view will appear in the map. 

{% include image.html src="docs/mapping_mode/mapillary.png" alt="Display Mapillary imagery" title="Display Mapillary imagery" %}

Click in any of the green points available to see the street view imagery. Try to see the element of interest (in this case the building) and update the information needed.

{% include image.html src="docs/mapping_mode/street_view.png" alt="Street View" title="Street View" %}

In our case, the building of interest is the pink one on the right side. From the picture is possible to classify the building type as "residential". In addition, it is possible to add the number of levels of the building. If the building usage is not homogeneous, the tag “building:use” can be given and filled with all usages (e.g. “residential, commercial”). 

{% include image.html src="docs/mapping_mode/fill_missing_tags.png" alt="Fill the missing tags" title="Fill the missing tags" %}

After you finished editing, just go to the saving button in the top right corner and add a description of the changes made including the sources where you got the information. Don’t forget to use our hashtag <b>#goatmuc</b> for mapping activities in Munich, <b>#goatffb</b> for Fürstenfeldbruck and <b>#goatfr</b> for Freising.

{% include image.html src="docs/mapping_mode/osm_save_changes.jpg" alt="Save your changes" title="Save your changes" %}

If you now go back to the OSM Mapping Mode of GOAT, you will see in around 10 minutes that the task for this building is completed.