# Geoserver: caching
Here is my recipe to set up caches for geoserver.

Step 1: Planning

The client software (eg. OpenLayers) makes a request to geoserver, such as: 'give me an image, for layer L, covering area A'. Geoserver creates an image corresponding to this definition and send it back to the client.
Caching the results means that a series of requests are prepared in advance.
For that, you must know at least:

* The dimensions (width, height) of the output image;
* The size of the tiles you want to receive to fill up the image;
* Predefine a series of zoom levels;

Let's say we want the map's dimensions to be width=900px and height=450px. I'll display a global view of countries, from 0° to 360° and -90° to 90°, in EPSG:4326 (plate carrée).

Step 2: Setting up a grid in geoserver

Step 3: Configuring the client

Step 4: Checking your are really hitting the cache
