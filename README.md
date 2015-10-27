# week8
Three approaches for creating custom basemaps  

##Start up your VM!
https://gis5574.signin.aws.amazon.com/console)  

## Preamble
In the early days of web mapping, customizing the basemap was a time consuming and rather difficult process. Today, circumstances have changed and there are several ways to build a custom basemap. As you think about your projects, consider what sort of basemap you want and which of the techniques below to utilize.

## Assignment
A "rough draft" of a basemap that is customized for your project. You'll likely only need one basemap for your project in the end, but starting out **I'd like each person to make one**. Next week we'll take some group time to look at one another's work and come to a consensus regarding basemap style. I'm guessing you may like aspects from several maps and will in the end create a comprehensive basemap as a group (or at least, a designated group member).

## The available methods (no particular order)

### Using ArcMap
There are a lot of resources for using ArcMap. It gives you nearly complete control, and for those of us with GIS training, is a familiar interface to use. Basically, you'll in effect create a different map for each zoom layer you want to create tiles for and use scale ranges to create a seamless, unified experience for your users. Your basemap is published on ArcGIS Server and sliced up into a tile cache for serving. With this approach, table of contents organization is paramount. Otherwise it's easy to go nuts trying to keep track of the multiple copies of the same underlying data.

- http://blogs.esri.com/esri/arcgis/2008/03/17/working-with-layers-and-scale-ranges-tips-for-organizing-the-table-of-contents/
- http://blogs.esri.com/esri/arcgis/2011/06/24/designing-operational-overlays-for-the-arcmap-and-arcgis-online-basemaps/
- http://blogs.esri.com/esri/arcgis/2011/08/05/creating-a-web-map-service/
- http://blogs.esri.com/esri/arcgis/2011/08/04/cartographic-design-for-web-maps/

For a more in-depth lesson, see this [link](https://www.e-education.psu.edu/cloudGIS/node/47) as well as this [one](https://www.e-education.psu.edu/cloudGIS/node/49).

For an example, look at the [UMN Campus History application](https://www.lib.umn.edu/apps/campushistory/). If you zoom in pretty far, you'll see the basemap shift to a uglier, more simple gray basemap. That's a custom one I made very quickly because we needed that level of coverage.

### Using Mapbox Studio Classic
[Download](https://www.mapbox.com/mapbox-studio-classic/) and install onto your virtual machine. You'll need to create a Mapbox account to use it (it's free and they don't ask for a bunch of information) Mapbox Studio allows you to integrate data (called Sources) and style that data using CartoCSS. Since you have a great array of styles to start from and customize (rather than starting totally from scratch), once you get used to CartoCSS Mapbox Studio is (I think) a speedier option compared to ArcMap. Also, Mapbox handles hosting and serving of your tiles, which can sometimes be a headache with the ArcMap approach.

- https://www.mapbox.com/guides/source-quickstart/
- https://www.mapbox.com/guides/source-manual/
- https://www.mapbox.com/guides/style-quickstart/
- https://www.mapbox.com/guides/style-manual/

### Using Google Maps API
Perhaps the fastest way to work with a styled basemap. You can't create your own basemap wholesale, but can customize what points of interest you want displayed and the color/styling. When using the Google Maps API, note that you need an API key. For your convenience, you can use the following key: `AIzaSyBoE3QwsVadgmw0_XaZ-z73oAniNltqo50`. I've included index.html with an example of styling the Google Basemap (from this [tutorial](https://developers.google.com/maps/documentation/javascript/examples/maptype-styled-simple)).

- https://developers.google.com/maps/documentation/javascript/tutorial
- https://developers.google.com/maps/documentation/javascript/styling
