# IDE Requirements
AIMSICD can be build using any IDE that supports Android projects currently I use Intellij IDEA as my chosen IDE for Android development but others such as Eclipse or Android Studio would also be fine.

# Required Libraries
Due to the nature of AIMSICD and the attempts at accessing OemRil methods additional java class files are required to access methods hidden in the standard Android SDK. Stripped down versions of the full frameworks and telephony class files have been included to allow accessing these hidden methods without the need for reflection. 

The screenshot below provides an easy explanation of how these libraries should be setup within your IDE, this screen is exactly the same in Android Studio and I believe very close to the Eclipse screen as well. Both libraries need to be above all other libraries to ensure their declarations of the hidden methods are used within the IDE but also must not be set to compile or be included within the project as they will be provided by Android, their inclusion is simply to allow access to the hidden methods within the IDE.
![IDE Modules setup](http://i59.tinypic.com/jghy5j.jpg)

# APK Signing
As AIMSICD shares the com.android.phone process it requires the apk to be signed using the AOSP platform key and to be installed as a system app (priv-app in KitKat) to function correctly and share the phone process.

**AOSP Platform keys**<br />
The AOSP platform keys can be found within the [Build Repo](https://android.googlesource.com/platform/build/+/master/target/product/security/) and you will require the two platform keys:<br />
<ol>
<li><a href=https://android.googlesource.com/platform/build/+/master/target/product/security/platform.pk8>platform.pk8</a></li>
<li><a href=https://android.googlesource.com/platform/build/+/master/target/product/security/platform.x509.pem>platform.x509.pem</a></li>
</ol>

**Signapk.java**<br />
To sign the apk the java file [Signapk.java](https://android.googlesource.com/platform/build/+/master/tools/signapk/SignApk.java) is required which is also contained within the Build Repo under tools then signapk.

**How to Sign the APK**<br />
`java -jar signapk.jar platform.x509.pem platform.pk8 ORIGINAL-APK-NAME.apk SIGNED-APK-NAME.apk`