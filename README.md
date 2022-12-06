# About

> :warning: **DISCONTINUATION OF PROJECT** - 
> *This project will no longer be maintained by Intel.
> Intel has ceased development and contributions including, but not limited to, maintenance, bug fixes, new releases, or updates, to this project.*
> **Intel no longer accepts patches to this project.**
> *If you have an ongoing need to use this project, are interested in independently developing it, or would like to maintain patches for the open source software community, please create your own fork of this project.*

This is a general purpose visualization tool for OCCI Entity instances. 
OCCI Resource entities are visualized as points on a round wheel, while the Link entities connecting the Resources are depicted as colorful lines between them.
 
This web application consists of two parts: (a) **the OCCI diagram/map**, (b) the **OCCI visualization web application**. 
 
This project has been developed by [Gregory Katsaros](mailto:gregory.katsaros@intel.com), Cloud Services Lab, Intel Labs Europe, and is  distributed under the Apache License, Version 2.0. 


## OCCI diagram/map

The OCCI diagram/map is web page developed using the [d3.js](http://d3js.org/) library and is consisted of two files: *occi_diagram.html*, *occi_digrama.css*. The OCCI diagram can be used also independed from the rest web application and, thus, be integratged within other platforms/websites. 
     
The Links representation and the OCCI data source can be customized by editing the *occi_diagram.html*:
            
    //link styles initialization
    //The format of the following object is: source_resource_term:style_class
    var linkstyles = { "agreement":"agreementlink", "storage":"storageink"};
    //url initialization
    var base_server_url = "data.json"; //default local dataset. The URL of the OCCI enabled server can be used also: e.g. http://ServerNameOrIPAddress:port
    var search_term = "";
        

This OCCI resource visualization will work with any OCCI compliant server as long as it supports a JSON rendering. 
The respective style classes must be present in the occi_diagram.css. E.g.: 

    .compute {
    font: 300 11px "Helvetica Neue", Helvetica, Arial, sans-serif;
    fill: #FF0000;
    }
    .network {
    font: 300 11px "Helvetica Neue", Helvetica, Arial, sans-serif;
    fill: #886A08;
    }
              

You can preview the OCCI diagram/map [here](http://bl.ocks.org/gkatsaros/a0a43032c4b50a246d4d).          
     
## OCCI visualization web application
    
The OCCI web application is a set of html, css and js files that work as a "wrapper" around the OCCI diagram/map. Is shows how the map can be integrated within a web platform.
This web application has been developed using the [Bootstrap framework](http://getbootstrap.com/) in order to achieve a responsive web application experience. 
   
## Graphics

The icons included in the specific project have been distributed by The [Noun Project](http://thenounproject.com/) under the Creative Commons (CC BY 3.0) license.
    
 Specifically this software includes components that are released under the following licences:
* bootstrap.js, bootstrap.min.js, bootstrap-select.js, jQuery, fonts (glyphicons-halflings-regular): MIT License (MIT)
* d3.js: BSD License
* Computer node: Creative Commons - Computer designed by Simple Icons from the Noun Project
* Agreement node: Creative Commons - Quote designed by Yazmin Alanis from the Noun Project
* Network node: Creative Commons - Network designed by Edward Boatman from the Noun Project
* Storage node: Creative Commons - Hard Drive designed by Oleg Frolov from the Noun Project
