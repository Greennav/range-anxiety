# range-anxiety

Computation and visualization of the vehicle's range.

Given initial Latitude and Longitude, or OSM Node Id, and range value, outputs a list of nodes forming the edges of a [polygon](https://gist.github.com/bfmags/6cd82eaf4270a9657ff7b1301e51d574) or a group of [markers](https://gist.github.com/bfmags/6a7ef7cfd080460e3c18578476bbcae4), with a rest endpoint for both requests.
If sucessful, the API will return a JSON Object following the [GeoJSON](http://geojson.org/) format specification.

See below for examples of how to use the API.

### Prerequisites
#### Install the latest version of JDK and Maven

### Setup

Clone and navigate to the directory range-anxiety.

```
$ mvn package
$ cd target
```

Move the Jordan.osm.pbf file to the target folder.

### Run

```$ java -jar range-1.0-SNAPSHOT.jar```

### Working Example

Examples below use Jordan.osm.pbf for the map data.
Returns valid JSON output that can be used directly in any map editor without any further rearrangement.

To get the polygon format, using either lng/lat or OSM Node Id parameters.

* ```http://localhost:8111/greennav/polygon?startlat=31.7239898&startlng=35.6429683&range=10.0```
* ```http://localhost:8111/greennav/polygon?startNode=3602680930&range=10.0```


To get the marker format, using either lng/lat or OSM Node Id parameters.

* ```http://localhost:8111/greennav/marker?startlat=31.7239898&startlng=35.6429683&range=10.0```
* ```http://localhost:8111/greennav/marker?startNode=3602680930&range=10.0```

______

For more details, read 'FinalReport.pdf' available in the docs folder. 
