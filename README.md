## Raster to Polyline conversion

A simple and efficient script for converting rasters to polyline shapefiles, comparable to the `RasterToPolyline` tool in ArcGIS, or `r.thin` and `r.to.vect` in GRASS GIS, except it only requires GDAL as a dependency.

It assumes raster values of 1 define lines (ignoring all other values), applies a thinning algorithm to skeletonize the network, and then converts the remaining skeleton to an ESRI shapefile.

The thinning algorithm implemented can be found in the following reference ("Algorithm B"):

	"Analysis of Thinning Algorithms Using Mathematical Morphology" by Ben-Kwei Jang and Ronlad T. Chin in Transactions on Pattern Analysis and Machine Intelligence, vol. 12, No. 6, June 1990.

### Usage

Download this script and make sure it's in your path. Then:

```
from RasterToPolyline import RasterToPolyline

RasterToPolyline("/path/to/my_raster.tif")
```

That's all there is to it. I hope someone finds this useful.


### Acknowledgement

This script was developed during an internship with [OpenTopography](https://opentopography.org/), which receives support under the following U.S. National Science Foundation award numbers: 1948997, 1948994, 1948857.
