---
title:  "Testing innovative data collection approaches"
author: [ramirez, jehle, pajares]
lang: en
tags: [en]
categories: [news]
thumbnail: blog/sensor_freiberg/plots.png
image: blog/sensor_freiberg/plots.png
excerpt: How does the GOAT-team come to a project for on-street delivery robots? Of course we share the same walking and cycling environment. We have been using a prototype measuring box to automatically detect collect surface and smoothness information of road infrastructure. 
---
Imagine you are coming out of your house to pick up your food delivery or your Amazon purchase, and surprise! 
Wall-E! What? Well, not exactly. But it may be an autonomous robot making the delivery one day in the future. Wait, weren’t autonomous vehicles something reserved for cars, trains, or trucks? NO, autonomous vehicles come in the different sizes. However, as every self-driving vehicle, they are facing one of the biggest challenges to fully operate: the awareness of the environment where they are moving. For that reason, the team of Prof. Sebastian Zug at the [Chair for Software Technology and Robotics of TU Bergakademie Freiberg](https://tu-freiberg.de/fakult1/inf/professuren/softwaretechnologie-und-robotik) is working on the [project “AK hoch 2“](https://www.bmvi.de/SharedDocs/DE/Artikel/DG/mfund-projekte/akhoch2.html) which is currently funded by the Federal Ministry of Transport and Digital Infrastructure, to measure the quality and characteristics of the bicycle infrastructure. Specifically, the goal of the project is to systematically aggregate the parameters of cycleways and footpaths. To achieve it, they created a mobile measuring system that can be setup on any bicycle, evaluates motion sensors and combines them with position information. Finally, an AI-based classification identifies the type and smoothness of the surface and thereby locates obstacles.

{% include image.html src="blog/sensor_freiberg/sensors.png" alt="measuring system" maxheight="400px" %} 
<i>Figure 1. The measurement box developed by the TU Bergakademie Freiberg</i>

How does the GOAT-team come to a project for on-street delivery robots? Of course we share the same walking and cycling environment. As the main goal of the project is to collect information for cycling and walking infrastructure, we share very important common interest: reliable and accurate spatial data. For that reason, we have been using the prototype measuring box in our field mapping tasks to collect the information. Here is a sneak peek going around Munich’s Streets.

{% include image.html src="blog/sensor_freiberg/cyclepath.png" alt="cyclepath captured with the measuring devise" maxheight="400px" %} 
<i>Figure 2. Exemplary cycling route that was captured with the measuring devise</i>

The device shows the route ridden, and the user must continuously indicate the category of the infrastructure that he is using (street, bike-way or pedestrian path). Then the GNSS position is harmonized by a MapMatching algorithm, which compares the derived location with the information available in OpenStreetMap. But the sensor is way more than just GNSS and Speedometer.

{% include image.html src="blog/sensor_freiberg/plots.png" alt="acceleration plots" maxheight="400px"%} 
<i>Figure 3. Measured acceleration in all three dimensions </i>

The sensor has an accelerometer that is continuously measuring changes in all three axes plus the vector sum of them. From the acceleration charts it is possible to identify certain behaviors as acceleration and braking from the changes in the X-axis where below zero would mean breaking and over zero is accelerating. Likewise, in the Y-axis it is possible to identify a constant vibration, however some larger spikes appear in the graph and they may be related to bumps or a rough surface. Finally, and related to the Z-axis, it could be possible to identify sharp changes in the horizontal alignment of the infrastructure or obstacles that may not allow a smooth ride. 

Remember [our experience with Mapillary in Fürstenfeldbruck](../mapillary)? This time we used the same process to have both the collection of acceleration data, and the street pictures with intervals of 1 second to have a better understanding of the road conditions. These first results are very promising and we are looking forward to further use the device in our efforts for more better map data.


