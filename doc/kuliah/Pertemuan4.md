Background :
Geospatial data is a science that studies based on the coordinates of a map or can also be said to be studying the geographic found on the earth's surface. In the geospatial data we can manipulate data and calculate record on file.shp, and in that there is a basic file file.shp ie shapefiles. In this shapefile there file.shp with file.dbf, where to read shapefiles we can use python and dial directly file.shp or can also create a class first.

discussion:
Retrieve geospatial data is one way to select / view, the data record of file.dbf and geometry of file.shp. File.dbf itself an attribute of a table of data, while file.shp the geometry data in shapefile.

ESRI standard geometry:
Point
Poliline
Polygon
How to read the number of operations on the geometry data using python:
Dial the library pyshp manner = shapefile import.
Then do instansiansi class shapefile to a variable, as shown below the following example:

From the picture above can be seen that the instant of the class sf shapefiles and we can invoke a method in the instant variable sf.
Next create sf.shapes ()
Then make a = sf.shapes ()
Recently typing len (a)
How to read data operations on DBF using python:
Dial the library pyshp manner = shapefile import.
Then do the calling of all data records in a way = sf.records ().
Last did beriske -n record retrieval by way = sf.record (n).
Method used in shapefile:
Some of the data contained in file.shp are as follows:
BBOX (Bonding box) = data based on a 4 point coordinate pingir view of a folder.
Parts = a recording apps that are part of another record.
Points = is forming coordinate geometry data.
Shape Type = shape type used is ESRI standard.
conclusion:
In retreive geospatial data we can select or view and counting the number of data records. One way we can do by performing operational python.

Suggestion :
In the future we should be able to implement it and to understand it in detail, in order to facilitate the work or activities related to geospatial data.
