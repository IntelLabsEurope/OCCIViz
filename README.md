# About

This is a general purpose visualization tool for OCCI Entity instances. 
Through this application the OCCI Resource entities are being visualized as points on a round wheel, while the Link entities connecting the Resources are being depicted as colorfull lines between them.

This web application is consisted of two parts: (a) **the OCCI diagram/map**, (b) the **OCCI visualization web application**. 

This complete project have been developed by Gregory Katsaros, Intel, Cloud and Services Lab, and is being distrbuted under Apache 2.0 license. 


## OCCI diagram/map

The OCCI diagram/map is web page developed using the [d3.js](http://d3js.org/) library and is consisted of two files: *occi_diagram.html*, *occi_digrama.css*. The OCCI diagram can be used also independed from the rest web application and, thus, be integratged within other platforms/websites. 
     
The Links representation and the OCCI data source can be customized by editing the *occi_diagram.html*:
            
    //link styles initialization
    //The format of the following object is: source_resource_term:style_class
    var linkstyles = { "agreement":"agreementlink", "storage":"storageink"};
    //url initialization
    var base_server_url = "data.json"; //default local dataset
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
                        
     
## OCCI visualization web application
    
The OCCI web application is a set of html, css and js files that work as a "wrapper" around the OCCI diagram/map. Is shows how the map can be integrated within a web platform.
This web application has been developed using the [Bootstrap framework](http://getbootstrap.com/) in order to achieve a responsive web application experience. 
   
## Graphics

The icons included in the specific project have been distributed by The [Noun Project](http://thenounproject.com/) under the Creative Commons (CC BY 3.0) license.
    
The following icons have been used:
* Computer node: Creative Commons - Computer designed by Simple Icons from the Noun Project
* Agreement node: Creative Commons - Quote designed by Yazmin Alanis from the Noun Project
* Network node: Creative Commons - Network designed by Edward Boatman from the Noun Project
* Storage node: Creative Commons - Hard Drive designed by Oleg Frolov from the Noun Project
