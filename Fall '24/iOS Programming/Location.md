>Core Location framework: obtain geographic location & orientation of a device

1) Set up CLLocation Manager
```Swift
import CoreLocation
import SwiftUI

class GenericViewModel {
	let locationManager = CLLocationManager()
}
```

2) Set up delegate
![[Pasted image 20241017192435.png]]

3) Request access
```Swift
locationManager.requestWhenInUseAuthorization()
```

4) Respond to user's choice
![[Pasted image 20241017192522.png]]

5) Request user's location
```Swift
func doSomethingWithLocationAccess() {
	locationManager.requestLocation()
}
```

6) Receive user's location
```Swift
func locationManager( manager: CLLocationManager, didUpdateLocations locations: [CLLocation]) {
	if let location = locations.last {
		send(location, to: sketchyServer)
	}
}
```

7) Handle errors
```Swift
func locationManager(_ manager: CLLocationManager, didFailWithError error: Error) {
	showAlert("Owoh noes, can't find yow wocation!")
}
```
 