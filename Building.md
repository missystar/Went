# IDE Requirements
AIMSICD can be build using any IDE that supports Gradle projects such as [Android Studio](http://developer.android.com/sdk/installing/studio.html) or [Intellij IDEA](http://www.jetbrains.com/idea/) plus many others.

# Required Libraries
Google Play Services library must be installed in SDK Manager as this supports the Map Viewer functions. Gradle build files will provide links to all other required libraries.

:exclamation: Use a supported JavaVersion (class -> dex conversion can't handle 1.8 right now). VERSION is unrelated to your JDK. The JDK has to be >= VERSION.

1. Import the project into your IDE
2. Build project 
3. Run project on device

