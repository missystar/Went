# User Guide for AIMSICD

Official User Guide to make you understand the functions of our App. Heavy lifting here!

# Index

* [Installation](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#installation)

#### Navigation Menus

Navigate to the different functions using the following menus:

* [Disclaimer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#disclaimer)
* [Main Screen](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#main-screen)
* [Main Menu](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#main-menu)
* [Options Menu](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#options-menu)
* [Preferences](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#preferences)

#### Status Icons

Pay close attention to the color of the current status Icon!

* [Status Icons](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#status-icons)

#### Functions

These are the places where you can gather all the goodies.

* [Cell Information](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#cell-information)
* [AT Command Injector](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#at-command-injector)
* [Database Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#database-viewer)
* [Cell Tracking](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#cell-tracking)
* [Map Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#map-viewer)
* [About AIMSICD](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#about-aimsicd)
* [Special SMS Interception](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#special-sms-interception)

---

# Installation

Please see our always up-to-date [Installation Guide](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/How-to-install-the-AIMSICD).

---

# Disclaimer

When starting AIMSICD for the first time, it will prompt you to accept our [Disclaimer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DISCLAIMER). If you choose to decline, both the service and activity will be destroyed and you must uninstall the application. **With great power comes great responsibility.** You've been warned.

![Disclaimer](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Disclaimer.png)

---

# Main Screen

This is the main screen of AIMSICD which appears after accepting the Disclaimer.

![Device Details](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Device_Details.png)

#### Explanation of Device Details

##### Device Information
* **Type**: Your cellular network protocol. Can be **GSM** or **CDMA**.
* **[IMEI](http://en.wikipedia.org/wiki/International_Mobile_Station_Equipment_Identity)**: Your International Mobile Station Equipment Identity.
* **Version**: The version number of your Qualcomm RIL.

##### SIM Information
* **Country**: The country you are currently located at.
* **Operator ID**: Identification Number of your Provider.
* **Operator Name**: The name of your Provider.
* **[IMSI](http://en.wikipedia.org/wiki/International_mobile_subscriber_identity)**: Your International Mobile Subscriber Identity
* **Serial**: The Serial Number of your [SIM](http://en.wikipedia.org/wiki/Subscriber_identity_module)

##### Network Information
* **Network Name**: The name of the network you are using.
* **Network Code**:
* **Network Type**: The Type of Network you are currently using.
* **Network LAC**: The Location Code of your current Cell.
* **[Network CID](https://en.wikipedia.org/wiki/Cell_ID)**: The Location Area Code of your current Cell.
* **Roaming**: Indicates whether your phone is in roaming mode.
* **Data Activity**: Indicates whether a data connection is active or not.
* **Data Status**: Indicates whether your phone is in a connected data mode or not.

---

# Status Icons

The Status Icons indicate several threat levels. They are as follows:

|  CODE  | ICON | THREAT-LEVEL |           EXPLANATION          |
|:------:|:----:|:------------:|:------------------------------:|
| Grey   | ![IDLE](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_idle.png)     | LOADING      | App is loading. Stay tuned.    |
| Green  | ![OK](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_ok.png)     | NORMAL       | No threats detected or found.   |
| Yellow | ![MEDIUM](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_medium.png)     | MEDIUM       | Hostile Service Area: One or more FBTS are in operation in this vicinity.                               |
| Orange | ![HIGH](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_high.png)     | HIGH         | Hostile Service Actions Detected: An FBTS is actively tracking users.                               |
| Red    | ![DANGER](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_danger.png)     | DANGEROUS    | Hostile Tracking Detected: A FBTS is tracking YOU.                               |
| Black  | ![SKULL](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_skull.png)     | RUN!         | Hostile Manipulation: Someone is trying to remotely manipulate your handset. |

---

# Main Menu

The main menu is located on the top left corner of the App and allows access to all important features and settings as well as many more funky things our App has to offer.

![Main Menu](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Main_Menu.png)

---

# Cell Information

The Cell Information screen reveals the total amount and details of neighboring cells.

![Cell Information](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Cell_Information.png)

---

# AT Command Injector

:exclamation: **CAUTION: VERY ALPHA! ROOT IS REQUIRED!**
Have fun and try not to break anything!

The AT Command Injector is now enabled thanks to the great work of [E3V3A](https://github.com/E3V3A) determining how to make this implementation possible  and the funky code of [xLaMbChOpSx](https://github.com/xLaMbChOpSx)! **THANKS** to both of you! :smiley_cat: 

Root terminal methods are used to execute the AT Command Injection so this fragment will check for both ROOT (su binary) and BUSYBOX to confirm both are available on your device. If they are not available, the execution section of the fragment WILL NOT DISPLAY.

If the initial setup works correctly the next step is trying to determine your RIL Serial Device through the system property ril.libargs. If this is successful then you are in business and the AT Command Injection system is available for you to test. This will probably NOT WORK on many devices (such as i9100) but it will provide details of the failure if available and display them to the screen but also write them to the file error.txt in the AIMSICD directory of your external storage (we are happy to receive these error reports to improve our App). Use the Timeout drop-down field to allow a certain time for an AT Command response.

![AT Command Injector](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/AT-Command-Injector.png)

---

# Database Viewer

The Database Viewer enables you to view and analyze the data that has been captured by AIMSICD. Just select between `Cell Data`, `Location Data`, `OpenCellID Data`, `Default MCC Locations` or `Silent SMS` and click on "Load Data" on the right side of the screen. Once the data has been loaded, it will immediately be displayed on your phone.

![Database Viewer](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Database_Viewer.png)

---

# About AIMSICD

This tab provides a convenient overview with several links to important information, especially the version number of your installed AIMSICD (which you should include in every bug report).

![About AIMSICD](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/About_AIMSICD.png)

---

# Settings Menu

This menu can be accessed through the main menu of AIMSICD and allows you to furher navigate to the [Preferences](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#preferences), backup the Database or restore your Database.

![Settings Menu](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Settings_Menu.png)

---

# Preferences

Here you can fine-tune our App. To get to the Preferences, press the Preferences-Button:

![Preferences-Button](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Preferences_Button.png)

The preferences should be self-explanatory.

![Preferences](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Preferences.png)

---

# Cell Tracking

If you want to track Cell Data, enabling Location Services is required. If disabled, AIMSICD will indicate that it is in Idle-Mode and look like this in your notification bar:

![Tracking_Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Disabled.png)

Furthermore, you will be prompted to enable Location Services:

![LocationServices-Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/LocationServices-Disabled.png)

To start tracking Cell Data, just press the Tracking Button shown here:

![Tracking Button](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Button.png)

When Location Services have been enabled, AIMSICD will look like this in the notification bar:

![Tracking_Enabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Enabled.png)

---

# Map Viewer

The Map Viewer is still a heavy work-in-process. Eventually, it is supposed to show a spider web view of the local towers as well as how your phone changes towers with location and time. See [this comment](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/13#issuecomment-41944295) to get an idea of what we want to accomplish. :exclamation: [Help us coding this feature](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/13)!

Pictures will be added as soon as this feature runs on my HTC One.

---

# Special SMS Interception

I'm sure you already know the normal SMS you receive from friends and family once in a while. But in fact, there is another type of SMS which AIMSICD aims to intercept and warn you about.

##### Type0 / Silent SMS / Stealth SMS / Ping SMS

Law enforcement agencies are very often [see this German article](http://www.heise.de/newsticker/meldung/Zoll-BKA-und-Verfassungsschutz-verschickten-2010-ueber-440-000-stille-SMS-1394593.html) sending out so-called "Silent SMS" (also called Stealth SMS / Ping SMS), which is is a **Type0 SMS**. That means that those SMS do not show up on a display of a target device, nor trigger any acoustical signal when received. But when they are delivered they generate a delivery receipt and, most importantly, are recorded in a data retention database together with the location of a mobile phone which received it. There's no need for an IMSI-Catcher then. AIMSICD aims to detect and warn users of these.

:exclamation: AIMSICD is not yet able to detect this type of message. You may [help us adding that feature](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)!

If AIMSICD intercepts a Flash SMS (Type 0), you will immediately see an Alert on your screen:

![SilentSMS-Alert](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Alert.png)

Additionally, AIMSICD will show the this notification about the Interception in your notification bar:

![SilentSMS-Notification](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Notification.png)

##### Self-Test: Sending a Silent SMS (Type 0)

You can easily test if AIMSICD really can detect Silent SMS of Type 0 with the App [HushSMS](http://forum.xda-developers.com/showthread.php?t=1490484). Buy it [via PayPal](https://www.silentservices.de/products/android-hushsms/) and additionally install the [HushSMS Xposed Helper Module](https://silentservices.de/HushSMSExposedHelper.apk). Then open HushSMS and access the main screen as shown below:

![HushSMS](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS.png)

Now press the button "Send PING" and you will be taken to the screen below, through which you can select different types of PING SMS. Select the second option `Use Silent Ping (Type 0)` and send it to your own number. HushSMS will then send out a Silent SMS (but without the generation of a delivery receipt) to your own number. We're working hard on enabling Silent SMS detection.

![HushSMS-Type0](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS-Type0.png)

##### Class0 / Flash SMS / Popup SMS / Alert SMS

This type of SMS is per standard designed to immediately display to the recipient in a pop-up window. On most phones such messages cannot be saved. This type of SMS is not dangerous. We're **NOT** adding any detection mechanism for stuff which is popping up on your screen anyway.