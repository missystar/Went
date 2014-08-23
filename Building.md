## IDE Requirements
AIMSICD can be built using any IDE that supports the *Gradle* build tool, used by projects such as [Android Studio](http://developer.android.com/sdk/installing/studio.html) or [Intellij IDEA](http://www.jetbrains.com/idea/) plus many others. (*Gradle* is the new equivalent of the old "*Ant*" build tool.)

### Required Libraries
The *Google Play Services* library must be installed in SDK Manager as this supports the Map Viewer functions. Gradle build files will provide links to all other required libraries.

### General Procedure (if you have never build Android Java Apps before) for using Android Studio:
1. Download and install the JAVA SE Development Kit 7 (JAVA 8 is not yet supported) from [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html).
2. Install the latest *Android Studio* from [here](http://developer.android.com/sdk/installing/studio.html).
3. Follow the setup instructions [here](http://developer.android.com/sdk/installing/index.html?pkg=studio).
4. Add the required SDK pakages...

:exclamation: Use a supported JavaVersion (class -> dex conversion can't handle 1.8 right now). VERSION is unrelated to your JDK. The JDK has to be >= VERSION.

1. Import the project into your IDE
2. Build project 
3. Run project on device

