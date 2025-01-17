>Core Motion framework: process accelerometer, gyroscope, pedometer, and environment-related events

1) Set up a CMMotionManager
```Swift
import CoreMotion

let motionManager = CMMotionManager()
```

2) Check if motion data is available
```Swift
if motionManager.isDeviceMotionAvailable {
	// TODO: Start requesting the device's motion
} else {
	showAlert("Looks wike device motion is not avaiwabwle >w<")
}
```

3) Subscribing to device motion data
![[Pasted image 20241017193016.png]]

4) Clean up
```Swift
class GenericViewModel {
	// ...
	deinit {
		motionManager.stopDeviceMotionUpdates()
	}
}
```

![[Pasted image 20241017193105.png]]

 ## Purpose Strings
 >required for privacy-sensitive features to work
 >	==must be clear== 