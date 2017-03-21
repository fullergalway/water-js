# Water-JS

This is a fork of [Wind-js](https://github.com/Esri/wind-js) with some time element added by [Irish Marine Institute](http://www.marine.ie).

![Water JS](water-js.gif?raw=true "water-js")


This project is an experiment in client-side data processing and visualization. Most of the code in this project is taken from https://github.com/cambecc/earth and has been re-purposed to support easier application to a variety of mapping APIs and Frameworks.

## How it works

The code for this project uses nothing but an HTML5 Canvas element and pure Javascript. The data come from the Global Forecast System which produces a large variety of datasets as continuous global gridded datasets (more info below). The data is passed into a JS class called `Windy` which takes the bounds of the map, the data, and the canvas element and then applies a [Bilinear Interpolation](http://en.wikipedia.org/wiki/Bilinear_interpolation) to generate a smooth surface. Once the surface has been generated a function randomly places "particles" onto canvas at random x/y points. Each particle is then "evolved", moving in a direction and at a velocity that is dictated by the interpolated surface.

## The Demo

[http://fullergalway.github.io/water-js/](http://fullergalway.github.io/water-js/)

## The Data

### NetCDF

The example uses netcdf data, parsed using [netcdfjs](https://github.com/cheminfo-js/netcdfjs) and converted to the gfs json format in javascript.

### GFS

For more information about GFS data visit: [GFS Data](http://nomads.ncdc.noaa.gov/data.php?name=access#hires_weather_datasets).

Before GFS data can be used with this code it has to be converted into JSON. To do this we used another awesome project by @cambecc here [https://github.com/cambecc/grib2json](https://github.com/cambecc/grib2json). That tool converts data in the GRIB2 file format into a JSON structure with the grid represented as an array. An example result of that tool can be seen in the `gfs.json` file.

## Resources

* [https://github.com/Esri/wind-js]
* [https://github.com/cheminfo-js/netcdfjs]
* [https://github.com/cambecc/earth](https://github.com/cambecc/earth)
* [http://earth.nullschool.net/](http://earth.nullschool.net/)
* [GFS Data](http://nomads.ncdc.noaa.gov/data.php?name=access#hires_weather_datasets)
* [ArcGIS Developers](http://developers.arcgis.com)
* [twitter@esri](http://twitter.com/esri)


## Issues

Find a bug or want to request a new feature?  Please let us know by submitting an issue.

## Contributing

Esri welcomes contributions from anyone and everyone. Please see our [guidelines for contributing](https://github.com/esri/contributing).

## Credit

All the credit for this work goes to: https://github.com/cambecc for creating the repo: https://github.com/cambecc/earth. The majority of this code is directly taken from there, since it's utterly awesome.

## Licensing

This project inherits an MIT license from [cambecc/earth](https://github.com/cambecc/earth) because 95% of the code here was copied from that project.

A copy of the license is available in the repository's [license.txt]( https://raw.github.com/Esri/wind-js/master/license.txt) file.

[](Esri Tags: ArcGIS Web Mapping Visualization Wind Canvas Animation)
[](Esri Language: JavaScript)
