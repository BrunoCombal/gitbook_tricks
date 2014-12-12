# My Book

## Graticules
Open QGIS, and create a grid, using "Vector/Research Tools/Vector Grid".
Let's create a grid to wrap around the North pole:
xmin:-180°, xmax:180°, ymin:40°, ymax:85°. Set the X step to 10° and the Y step to 5°, and save the file as lines to a shapefile.

We will change the projection from EPSG:4326 ro EPSG:3995. For now, the shapefile has node only where the line horizontal and vertical lines intersect. After reprojection, the grid will look line a spider web. To have something closer to circles, we must add more points along each line, to have its re-proejcted shape closer to a circle. Just use, "Vector/Geometry tools/Densify geometry...", and just add 5 vertices (they will be added in-between existing nodes).

Now, it is time to reproject the grid to a polar project. Just open the processing tool box and search for "reproject", then select "Vector/general tools/reproject layer". Choose your target SRS (I set it to EPSG:3995, but you may prefer another projection), reproject, et voilà!



