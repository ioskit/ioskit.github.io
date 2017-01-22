---
layout: kit
name: 'MapKit'
iid: mapkit
status:
type: kit
since: iOS3
detailedUpdates:
 - update:
     ios: iOS7
     brief: "The Map Kit framework (MapKit.framework) includes numerous improvements and features for apps that use map-based information. Apps that use maps to display location-based information can now take full advantage of the 3D map support found in the Maps app, including controlling the viewing perspective programmatically. Map Kit also enhances maps in your app. See page content."
prefixe: 'MK'
abstract: "Contains classes for embedding a map interface into your application and for reverse-geocoding coordinates."
kits:
 - CoreLocation
links:
 - link:
     name: 'Location and Maps Programming Guide'
     url: https://developer.apple.com/library/ios/documentation/UserExperience/Conceptual/LocationAwarenessPG/Introduction/Introduction.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'MapKit Framework Reference'
     url: https://developer.apple.com/library/ios/documentation/MapKit/Reference/MapKit_Framework_Reference/index.html
     description: ' - Apple Developer'
     type: reference
 - link:
     name: 'MapKit Tutorials'
     url: http://www.raywenderlich.com/tag/mapkit
     description: ' - Ray Wenderlich'
     type: tutorial
---

The *MapKit* framework (`MapKit.framework`) provides a scrollable map that you can incorporate into your app’s user interface. Beyond just displaying a map, you can use the framework interfaces to customize the map’s content and appearance. You can flag points of interest using annotations, and you can use custom overlays to intersperse your own content with the map content. For example, you might use an overlay to draw a bus route, or use annotations to highlight nearby shops and restaurants.

In addition to displaying maps, the MapKit framework integrates with the Maps app and Apple’s map servers to facilitate directions. From the Maps app, users can delegate the providing of directions to any app that supports directions. Apps that provide specialized types of directions, such as subway routes, can register to provide those directions when asked. Apps can also request walking and driving directions from Apple servers and merge that route information with their custom directions to provide a complete point-to-point experience for the user.



###&nbsp;iOS 7

The Map Kit framework (MapKit.framework) includes numerous improvements and features for apps that use map-based information. Apps that use maps to display location-based information can now take full advantage of the 3D map support found in the Maps app, including controlling the viewing perspective programmatically. Map Kit also enhances maps in your app in the following ways:

* Overlays can be placed at different levels in the map content so that they appear above or below other relevant data.
* You can apply an MKMapCamera object to a map to add position, tilt, and heading information to its appearance. The information you specify using the camera object imparts a 3D perspective on the map.
* The MKDirections class lets you ask for direction-related route information from Apple. You can use that route information to create overlays for display on your own maps.
* The MKGeodesicPolyline class lets you create a line-based overlay that follows the curvature of the earth.
* Apps can use the MKMapSnapshotter class to capture map-based images.
* The visual representation of overlays is now based on the MKOverlayRenderer class, which replaces overlay views and offers a simpler rendering approach.
* Apps can now supplement or replace a map’s existing tiles using the MKTileOverlay and MKTileOverlayRenderer classes.
