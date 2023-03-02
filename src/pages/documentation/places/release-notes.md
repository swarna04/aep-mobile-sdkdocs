# Release Notes

## February 3, 2023

### Android Places 2.0.0

* Major version update for [Adobe Experience Platform Location Service](./index.md) for Adobe Experience Platform Mobile SDKs on Android compatible with Mobile Core 2.0.0. This library is now available as an [open source project on GitHub](https://github.com/adobe/aepsdk-places-android).

Please note that the following improvements have been made in the current release:

1. The `getNearbyPointsOfInterest` API without the errorCallback has been removed. Alternatively, use the below overloaded API which provides both successCallback and errorCallback:

```java
public static void getNearbyPointsOfInterest(final Location location,
      final int limit,
      final AdobeCallback<List<PlacesPOI>> successCallback,
      final AdobeCallback<PlacesRequestError> errorCallback)
```

2. The public classes `PlacesAuthorizationStatus`, `PlacesPOI`, and `PlacesRequestError` are consolidated under the `places` subpackage and require updating the import statements as shown below:

```java
import com.adobe.marketing.mobile.places.PlacesAuthorizationStatus;
import com.adobe.marketing.mobile.places.PlacesPOI;
import com.adobe.marketing.mobile.places.PlacesRequestError;
```