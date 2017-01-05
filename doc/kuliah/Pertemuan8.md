Background:

At last week's meeting we have discussed what are the things about Map Server. Let us remember that, MapServer is a freeware and open source application that allows us to display spatial data (maps) on the web. At this meeting we will discuss about how to install it from the Map Server.

discussion:

MapServer program in the form of CGI (Common Gateway Interface). This program will run on a web server, and based on certain parameters (especially in the form of a configuration file * .map) will generate data that will then be sent to a web browser, either in the form of a map or other image form.

How to install Map Server
To run the server folder, first run CentOS on a virtual box
Further connected to the host computer network virtualbox
After that, go to the root through the terminal
Then type in #install mapserver5 terminal
Wait until the installation is complete
After performing the steps above, then perform the installation Proxy Folders as follows:
Open a terminal type #install python-pip
Then type # python-dev
Then type #pip install mapproxy
Then type #install Vwsqi
After that, wait until the installation is complete
conclusion:
MapServer can be used to install itself on your computer and set up in a way that is good and right.
Suggestion :
Use Map Server applications because we can use and apply easily on our own computers.

This is how to install the map server in Linux
services:
  demo:
  tms:
    use_grid_names: true
    # origin for /tiles service
    origin: 'nw'
  kml:
      use_grid_names: true
  wmts:
    # use restful access to WMTS
    restful: true
    # this is the default template for MapProxy
    restful_template: '/{Layer}/{TileMatrixSet}/{TileMatrix}/{TileCol}/{TileRow}.{Format}'
    # and also allow KVP requests
    kvp: true
    md:
      # metadata used in capabilities documents for WMTS
      # if the md option is not set, the metadata of the WMS will be used
      title: Awangga GeoMap
      abstract: This is the Awangga GeoMap.
      online_resource: http://www.awangga.net/
      contact:
        person: Rolly Maulana Awangga
        position: Software Engineer
        organization: Belant Persada
        address: Jl. Ligar Nyawang No.2
        city: Bandung
        postcode: 40191
        country: Indonesia
        phone: +62(0)813-12000-300
        fax: +62(0)813-12000-300
        email: rolly@awang.ga
      # multiline strings are possible with the right indention
      access_constraints:
        This service is intended for Sekretariat Negara Only.
        The data is under development on Sekretarian Negara Republik Indonesia.
        (http://setneg.go.id/)
      fees: 'None'
  wms:
    md:
      title: MapProxy WMS Proxy
      abstract: This is a minimal MapProxy example.

layers:
  - name: agm
    title: Awangga Geo Map - www.awangga.net
    sources: [agm_cache]

caches:
  agm_cache:
    grids: [webmercator]
    sources: [agm_source]

sources:
  agm_source:
    type: mapserver
    req:
      layers: roads
      map: /var/mapdata/mapfile/agm.map
    coverage:
      bbox: [94.5011475, -11.007385, 141.01947, 6.076721]
      srs: 'EPSG:4326'
    mapserver:
      binary: /usr/libexec/mapserver
      working_dir: /var/mapdata/tmp
    supported_srs: ['EPSG:4326']

grids:
    webmercator:
        base: GLOBAL_WEBMERCATOR

globals: 

