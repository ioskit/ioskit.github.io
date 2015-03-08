---
layout: kit
name: 'MapKit'
id: mapkit
status: TODO
since: iOS3
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Map Kit framework (MapKit.framework) includes numerous improvements and features for apps that use map-based information. Apps that use maps to display location-based information can now take full advantage of the 3D map support found in the Maps app, including controlling the viewing perspective programmatically. Map Kit also enhances maps in your app. See page content."
prefixe: 'MK'
link: 
abstract: "Contains classes for embedding a map interface into your application and for reverse-geocoding coordinates. See MapKit Framework."
kits:
 - CoreLocation
links__:
 - link:
     name: 'aaa'
     url: bbb
     description: 'ccc'
---

Contains classes for embedding a map interface into your application and for reverse-geocoding coordinates. See MapKit Framework.


###&nbsp;iOS 7

The Map Kit framework (MapKit.framework) includes numerous improvements and features for apps that use map-based information. Apps that use maps to display location-based information can now take full advantage of the 3D map support found in the Maps app, including controlling the viewing perspective programmatically. Map Kit also enhances maps in your app in the following ways:

* Overlays can be placed at different levels in the map content so that they appear above or below other relevant data.
* You can apply an MKMapCamera object to a map to add position, tilt, and heading information to its appearance. The information you specify using the camera object imparts a 3D perspective on the map.
* The MKDirections class lets you ask for direction-related route information from Apple. You can use that route information to create overlays for display on your own maps.
* The MKGeodesicPolyline class lets you create a line-based overlay that follows the curvature of the earth.
* Apps can use the MKMapSnapshotter class to capture map-based images.
* The visual representation of overlays is now based on the MKOverlayRenderer class, which replaces overlay views and offers a simpler rendering approach.
* Apps can now supplement or replace a map’s existing tiles using the MKTileOverlay and MKTileOverlayRenderer classes.
