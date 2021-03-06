# @turf/shortest-path

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## shortestPath

Returns the shortest [path](http://geojson.org/geojson-spec.html#linestring) from [start](http://geojson.org/geojson-spec.html#point) to [end](http://geojson.org/geojson-spec.html#point) without colliding with
any [Feature](http://geojson.org/geojson-spec.html#feature-objects) in [ obstacles](FeatureCollection<Polygon>)

**Parameters**

-   `start` **Coord** point
-   `end` **Coord** point
-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** optional parameters (optional, default `{}`)
    -   `options.obstacles` **([Geometry](http://geojson.org/geojson-spec.html#geometry) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects) \| [FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects)&lt;[Polygon](http://geojson.org/geojson-spec.html#polygon)>)?** areas which path cannot travel
    -   `options.minDistance` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)?** minimum distance between shortest path and obstacles
    -   `options.units` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** unit in which resolution & minimum distance will be expressed in; it can be degrees, radians, miles, kilometers, ... (optional, default `'kilometers'`)
    -   `options.resolution` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** distance between matrix points on which the path will be calculated (optional, default `100`)

**Examples**

```javascript
var start = [-5, -6];
var end = [9, -6];
var options = {
  obstacles: turf.polygon([[[0, -7], [5, -7], [5, -3], [0, -3], [0, -7]]])
};

var path = turf.shortestPath(start, end, options);

//addToMap
var addToMap = [start, end, options.obstacles, path];
```

Returns **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[LineString](http://geojson.org/geojson-spec.html#linestring)>** shortest path between start and end

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/shortest-path
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
