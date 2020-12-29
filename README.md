# CodeLabGeoMap
In this codelab, you create the Wander app, which displays a Google map with custom styling. 
The Wander app allows you to drop markers onto locations, add overlays, and see your location in real time.

1)Add menu for map types
In this step, you add an app bar with an options menu that allows the user to change the map type.

To create a new menu XML file, right-click your res directory and select New > Android Resource File.
In the dialog, name the file map_options.
Choose Menu for the resource type.
Click OK.
In the Code tab, replace the code in the new file with the following code to create the map menu options. The "none" map type is omitted because "none" results in the lack of any map at all. This step causes an error, but you resolve it in the next step.

2)In the MapsActivity.kt file, find the onMapReady() method. Remove the code in it that places the marker in Sydney and moves the camera. This is what your method should look like now.

override fun onMapReady(googleMap: GoogleMap) {
   map = googleMap

}
Create a value for the latitude and a value for the longitude, and input their float values.

val latitude = 37.422160
val longitude = -122.084270
Create a new LatLng object called homeLatLng. In the homeLatLng object, pass in the values you just created.

val homeLatLng = LatLng(latitude, longitude)
Create a zoom value to decide how the map would look like
val zoomLevel = 15f


Styling the map
Step 1: Create a style for your map
Navigate to https://mapstyle.withgoogle.com/ in your browser.
Select Create a Style.
Select any style 
(google account required along with a key.
