---
title: Isochrone as Alphashape
permalink: /docs/alphashape/
---

GOAT allows you to calculate and visualize isochrones using alpha shapes. GOAT is using a very fast 2D concave hull algorithm [Concaveman](https://github.com/mapbox/concaveman) which was implemented in the paper  [A New Concave Hull Algorithm and Concaveness Measure for n-dimensional Datasets, 2012](https://journal.iis.sinica.edu.tw/paper/1/100295-3.pdf?cd=2217EEBB7C44EDA26). This alogirthm generates isochrones (polygons) representing the area from a set of points that can be reached in a dedicated time.
<td> {% include image.html src="docs/technical_documentation/alphashape/isochrone_as_alphashape.png" %} </td>

#### 1. Alphashape
Alpha shapes or α-shapes are often used to generalize bounding polygons around a given sets of points. Depending on the chosen alpha parameter the precision of the isochrone can differ. The following example illustrates how alpha shapes are generated depending on the alpha-parameter. 
##### 1.1. Points from the network
<td> {% include image.html src="docs/technical_documentation/alphashape/set_points.png" %} </td>

##### 1.2. Convex Hull 
In the first case is the α-parameter=0. This means that the form generated from the calculation resembles all data points. This is called convex hull. 
<td> {% include image.html src="docs/technical_documentation/alphashape/convex_hull.png" %} </td>

##### 1.3. Concave Hull
By decreasing the alpha parameter value, generated polygon will fit better the sample data. 
A Concave hull describes better the shape of the point cloud than the convex hull.  
<td> {% include image.html src="docs/technical_documentation/alphashape/concave_hull.png" %} </td>


<b><font color="red"> Different alpha parameters can be used for the calculation of the isochrones. However, GOAT uses a specific alpha parameter for the visualization of the isochrones in the frontend. 








