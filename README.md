# ndjson-to-geojson

Converts [newline delimited JSON](http://ndjson.org/) to a GeoJSON FeatureCollection:

- Each line will become a Feature,
- The `geometry` property of each line will become the Feature's `geometry`,
- The `id` property of each line will become the Feature's `id`,
- All other properties will be part of the Feature's properties.

Usage:

    cat file.ndjson | ./ndjson-to-geojson.js > file.geojson