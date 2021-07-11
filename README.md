# Fused-Location-API-Android
 How to use Fused Location API to fetch the current location in Android
 
 
####  Adding Permissions

To use location services, you need to add permission for location in the AndroidManifest.xml file. You can either use ACCESS_COARSE_LOCATION or ACCESS_FINE_LOCATION, based on your use:


<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
 
 
 #### ACCESS_COARSE_LOCATION 
 By adding this in your application, allows you to use WIFI or mobile cell data(or both) to determine the device’s location. The approximation by using this permission is close to the city level.
 
####  ACCESS_FINE_LOCATION:  
This uses your GPS as well as WIFI and mobile data to get the most precise location as possible. By using this, you will get a precise location of your user.

#### ACCESS_BACKGROUND_LOCATION:
This permission was introduced in Android 10. So, for Android 10 or higher, if you want to access the user's location in the background, then along with any of the above two permissions, you need to add the ACCESS_BACKGROUND_LOCATION permission also.


#### Add dependencies

In order to use the Fused Location API, you need to add the dependency of location. So, in your app-level build.gradle file, add the below dependency:



dependencies {
    ...
    implementation 'com.google.android.gms:play-services-location:17.0.0'
}



