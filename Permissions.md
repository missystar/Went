Our `Android IMSI-Catcher Detector` has tons of cool features, but you might be confused or worry why we need so [many permissions](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/development/AIMSICD/src/main/AndroidManifest.xml). The reason is simple: We need to overcome the Android OS limitations as described in our [Development Roadmap](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#development-roadmap). Since our App needs to digg down deep into the baseband and read values that are normally not readable, `AIMSICD` needs just about all variables, sometimes even ROOT access for extended functions like silent SMS detection. But don't worry, it is not mandatory and we're privacy enthusiasts - which means we're always trying to melt down the permissions to the bare necessities. Should you ever discover a permission you wonder about, feel invited to get in touch with us - either via E-Mail or a filed Issue. Thank you!

---

**XPrivacy**

If you use [XPrivacy](https://github.com/M66B/XPrivacy) (also on [XDA-Developers](http://forum.xda-developers.com/showthread.php?t=2320783)), **ONLY** restrict the following Permissions:

* Browser-Bookmarks
* E-Mail
* Calendar
* Contacts
* User Dictionary

Above restrictions have been tested thoroughly, but we do not guarantee AIMSICD to work as supposed to when restricting any Permissions. These values have been submitted to the [XPrivacy Crowd sourced restrictions](http://crowd.xprivacy.eu/). If you use the PRO-Version of XPrivacy, you can just download them automatically from the database of crowd sourced restrictions.

:exclamation: If you experience any Issues, completely disable XPrivacy first before reporting a bug! 