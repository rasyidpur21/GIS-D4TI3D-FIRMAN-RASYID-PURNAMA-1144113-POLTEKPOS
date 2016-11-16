Background :
As we have discussed in previous resume, in a geographic information system consisting of geospatial data contained within the vector data also raster data. In vector data we can create shapefiles or create shapefile data. Well on resume this time we will learn about how to make or mengcreate shapefile in the vector data. What it shapefile? How do I submit shapefile? What files are contained in the shapefile? How do I add a record? We consider all of these studies in the following discussion:

discussion:
Is a non shapefile format that is efficient and simple topology and serves as a storage container geometric location and attribute information from a geographic data. To make additions shapefiles we can use python and plugin pyshp.

How mengcreate shapefile using python:
'Import shapefile'
Incorporate variable initialization, a variable suppose to shapefile.writer it can be made with => 'a = shapefile.writer ()'
In mengcreate shapefile data, there are two formats used:
1. SHP => in SHP format, there are 3 types of shape file that is Point, Polyline and Polygon.
    Example: shp => a.point (x, y)
                                  a.poly [(x, y), (v, w)]

2. DBF => in DBF format there are three fields that are used. The first field contains the attributes of the table, while the second field contains the method used and the third field serves to save the shapefile name previously entered.
   Example: dbf => a.field ( 'name.field', 'c', '40')
        a.record ( 'bdg')
Geospatial data is stored using a method a.save ( 'file.shp').

Explanation of methods used:
Point (x, y): insert data in the form of paint into shp and all data must be formatted ESRI.1
Poly [(a, b), (c, d)]: polygon-shaped insert geospatial data (back to the starting point) or polyline (not back to point early).
Field ( 'name', 'c', '40'): it means making the polygon attribute table 'name' with varchar data type with a length of 40. This method can be repeated and can be done for kebuthan new field again.
Record ( 'Bandung'): fill the table with only one field value 'Bandung'.
Save ( 'nama.file'): save file to save the file.
How to add the Record:
On Point = 'a.point (x, y)' or 'a.point (x, y, 0,0)' with domain x and y are the coordinates
On polyline = 'a.poly (shapefile = 3 parts = [[[x1, y1, z1, w1], [x2, y2, z2, w2], [......]]])'
In Polygon = 'a.poly) shapefile = 5, parts = [[[.......], [.......]]])'
conclusion:
In making shapefile data create one that we can use is to wear a python and pyshp, because of the way the use that is simple enough to be understood so that it can be easy to implement.

Advice: Understand and make ourselves understood to the use and utilization of data shapefile, open just know so that we can easily implement it in the future.
