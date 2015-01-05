## IDE Requirements
AIMSICD can be built using any IDE that supports the *Gradle* build tool, used by projects such as [Android Studio](http://developer.android.com/sdk/installing/studio.html) or [Intellij IDEA](http://www.jetbrains.com/idea/) plus many others. (*Gradle* is the new equivalent of the old "*Ant*" build tool.)

### Required Libraries
The *Google Play Services* library must be installed in SDK Manager as this supports the Map Viewer functions. Gradle build files will provide links to all other required libraries.

### General Procedure using Android Studio:
(If you have never built an Android Java App before.)

1. Download and install some GitHub sync-tool like [SmartGit](http://www.syntevo.com/smartgit/) or [GitHub for Win/Mac](https://github.com/).  
2. Download and install the JAVA SE Development Kit 7 (JDK7) from [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html).
3. Install the latest *Android Studio* from [here](http://developer.android.com/sdk/installing/studio.html).
4. When you start Android Studio, you'll see "Welcome to Android Studio" with several options. Here you choose to *Open Project* and then navigate to your GitHub synchronization directory where you have added AIMSICD, from (1).  

![First AS load](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/MISC/AS_load_2.png)

This is especially true if you get an error message such as this one:

![Missing .idea Error](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/MISC/AS_error_1.png)

5. The project will open immediately, but now you want to *close* it, so that you can return to the Welcome screen, this time you choose **Configure >> SDK Manager**. Here you select all API's related to API 17, which is our lowest supported API.
6. For more details follow the setup instructions [here](http://developer.android.com/sdk/installing/index.html?pkg=studio).
7. Now click on the sideways *Gradle* tab, on the right side of the IDE. This will open a new window, once in it, double click on *assembleRelease*. Check for build errors in the lower screen log window.
8. If (7) copiles without errors, you can now build your own APK by clicking on the menu items: **Build >> Generate Signed APK**. This will ask you for 3 new passwords to be used in your "KeyStore" (1 master, 1 file, 1 APK alias). You may also add your credentials in [signing.properties](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/signing.properties) to enable [automatic signing](https://developer.android.com/tools/publishing/sign-auto).

![generatesignedapk](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/MISC/APK-Signing.png)

:cherries: If all of the above succeeded, push the App to your device and run.

---

:exclamation: **JAVA 8 is not yet supported.** Use a supported JavaVersion (`class -> dex` conversion can't handle 1.8 right now). VERSION is unrelated to your JDK. The JDK has to be >= VERSION.

---

### After Repository Refactoring and cleanup:
Apparently, the first time after you have added our repo using the (Windows) GitHub app, or deleted a previous version from Android Studio, you need to import it into Android Studio by:

* Selecting "**Import Non-Android Studio Project**"

Selecting "Open an existing Android Studio Project" doesn't work, as it doesn't seem to setup the .gradle and .idea files etc.


