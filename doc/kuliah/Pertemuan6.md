Background :
GIS or Geographic Information System is an information system that has data based on spatial data, or objects that are on the surface of the earth. In Geographic Information Systems, information technology is used to function as a tool that can assist in data storage, processing data, analyzing data, managing data and presenting information.
In the use of Geographic Information Systems shapefile data are used as the data format. Shapefile itself has several functions that can be used, one of which is the use of the editor. Editor itself is an editing process that is used in shapefile format.

discussion:
Editor is a function or process to do the editing in a shapefile. Examples delete road and Writer. Slightly reiterated Writer is a method used in shapefile to create a new shp file with .shp / .dbf.

The following steps are performed in the process editor:
Import shape file
Sf = shape file.editor (war.shp)
Sf.point (16,10,0,0)
Sf.record ( 'field')
Sf.save
Sf.save ( 'war.shp')
a = shapefile.reoder ( 'war.shp')
a.recorders ()
a.shapes (). points
a.shape () [0]
a.shape () [0] points
[(10,0,10,0)]

Next is an example of the process of delete the editor
Sf.delete (0)
a.shapes () [0] .points [(10,0,10,0)]
sf.points [16,10,0,0]
sf.record ( 'field')
sf.saver ( 'wr.shp')

conclusion:
In shapefile there are functions that are used to perform the editing process with .shp / .dbf, the process editor.

Suggestion :
It helps us to further deepen the knowledge of the SIG back especially functions that we apply to shapefile that can help us all in the future.
