# Location

## Get the last known location 
* Using the Google Play services location APIs, your app can request the last known location of the user's device.

**Set up Google Play services**
To access the fused location provider, your app's development project must include Google Play services. Download and install the Google Play services component via the SDK Manager and add the library to your project. 

**Create location services client**
In your activity's `onCreate()` method, create an instance of the Fused Location Provider Client as the following code snippet shows.

      private FusedLocationProviderClient fusedLocationClient;

      // ..

      @Override
      protected void onCreate(Bundle savedInstanceState) {
      // ...

      fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
      }

**Get the last known location**
Once you have created the Location Services client you can get the last known location of a user's device. When your app is connected to these you can use the fused location provider's `getLastLocation()` method to retrieve the device location.  

The following code snippet illustrates the request and a simple handling of the response:

      fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });