# User Guide for AIMSICD

Official User Guide to make you understand the functions of our App. This Guide is by far not complete and will most likely change quite a few times. Therefore, please bookmark it and come back once in a while.

# Index

* [Installation](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#installation)

#### Screens

Navigate to the different screens through swiping to the left or right with your fingers!

* [Disclaimer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#disclaimer)
* [Main Screen](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#main-screen)
* [Status Icons](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#status-icons)
* [Cell Information](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#cell-information)
* [AT Command Injector](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#at-command-injector)
* [Database Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#database-viewer)
* [About AIMSICD](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#about-aimsicd)
* [Options Menu](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#options-menu)
* [Preferences](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#preferences)

#### Functions

* [Cell Tracking](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#cell-tracking)
* [Map Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#map-viewer)
* [Special SMS Interception](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#special-sms-interception)

---

# Installation

Please see our always up-to-date [Installation Guide](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/How-to-install-the-AIMSICD).

---

# Disclaimer

When starting AIMSICD for the first time, it will prompt you to accept our [Disclaimer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DISCLAIMER). If you choose to decline, both the service and activity will be destroyed and you must uninstall the application. With great power comes great responsibility. You've been warned.

![Disclaimer](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Disclaimer.png)

---

# Main Screen

This is the main screen of AIMSICD which you see after accepting the Disclaimer.

![Device Details](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Device_Details.png)

#### Explanation of Device Details

##### Device Information
* **Type**: Your cellular network protocol. Can be **GSM** or **CDMA**
* **[IMEI](http://en.wikipedia.org/wiki/International_Mobile_Station_Equipment_Identity)**: Your International Mobile Station Equipment Identity
* **Version**:
* **Line Number**: Your phone number.

##### SIM Information
* **Country**: The country you are currently located at.
* **Operator ID**: Identification Number of your Provider.
* **Operator Name**: The name of your Provider.
* **[IMSI](http://en.wikipedia.org/wiki/International_mobile_subscriber_identity)**: Your International Mobile Subscriber Identity
* **Serial**: The Serial Number of your [SIM](http://en.wikipedia.org/wiki/Subscriber_identity_module)

##### Network Information
* **Network Name**: The name of the network you are using.
* **Network Code**:
* **Network Type**:
* **Network LAC**:
* **Roaming**: Indicates whether your phone is in roaming mode.
* **Data Activity**:
* **Data Status**:
* **Network CellID**:

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

# Cell Information

The Cell Information currently only shows you the number of neighboring cells.

![Cell Information](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Cell_Information.png)

---

# AT Command Injector

The AT Command Injector is not enabled yet as we are still working hard on figure out how to gain full AT access to the Baseband Processor. 

![AT Command Injector](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/AT-Command-Injector.png)

---

# Database Viewer

The Database Viewer enables you to view and analyze the data that has been captured by AIMSICD. Just select between Cell Data, Location Data, OpenCellID Data, Default MCC Locations or Silent SMS and click on "Load Data" on the right side of the screen. Once the data has been loaded, it will immediately be displayed on your phone.

![Database Viewer](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Database_Viewer.png)

---

# About AIMSICD

This tab provides a convenient overview with several links to important information, especially the version number of your installed AIMSICD (which you should include in every bug report). All links are self-explanatory.

![About AIMSICD](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/About_AIMSICD.png)

---

# Options Menu

This menu can be accessed through pressing on the three dots in the upper right corner of AIMSICD. You can either chose to navigate to the Preferences, the Database Viewer, backup the Database, restore the Database, update OpenCellID Data or Quit the App.

![Options Menu](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Options_Menu.png)

---

# Preferences

Here you can fine-tune our App. The preferences are self-explanatory. On the very bottom you can also select the style of the Icons that are displayed by AIMSICD - these can be either a style of "Flat", "Sense" or "White".

![Preferences](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Preferences.png)

---

# Cell Tracking

If you want to track Cell Data, enabling Location Services is required. If disabled, AIMSICD will look like this in your notification bar:

![Tracking_Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Disabled.png)

Furthermore, you will be prompted to enable Location Services:

![LocationServices-Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/LocationServices-Disabled.png)

To start tracking Cell Data, just press the Tracking Button shown here:

![Tracking Button](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Button.png)

When Location Services have been enabled, AIMSICD will look like this in the notification bar:

![Tracking_Enabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Enabled.png)

---

# Map Viewer

The Map Viewer is still a heavy work-in-process. Eventually, it is supposed to show a spider web view of the local towers as well as how your phone changes towers with location and time. See [this comment](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/13#issuecomment-41944295) to get an idea of what we want to accomplish. Help us coding this feature!

To open the Map Viewer, simply press the world map as shown below:

![Map Viewer](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Map_Viewer.png)

---

# Special SMS Interception

I'm sure you already know the normal SMS you receive from friends and family once in a while. But in fact, there is another type of SMS which AIMSICD aims to intercept and warn you about. Here's a short explanation:

##### Type0 / Silent SMS / Stealth SMS / Ping SMS

Law enforcement agencies are very often [see this German article](http://www.heise.de/newsticker/meldung/Zoll-BKA-und-Verfassungsschutz-verschickten-2010-ueber-440-000-stille-SMS-1394593.html) sending out so-called "Silent SMS" (also called Stealth SMS / Ping SMS), which is is a **Type0 SMS**. That means that those SMS do not show up on a display of a target device, nor trigger any acoustical signal when received. But when they are delivered they generate a delivery receipt and, most importantly, are recorded in a data retention database together with the location of a mobile phone which received it. There's no need for an IMSI-Catcher then. Reliable detection of silent SMS will be trivial to the usefulness of AIMSICD.

AIMSICD is not yet able to detect this type of message. You may [help us adding that feature](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)!

If AIMSICD intercepts a Flash SMS (Type 0), you will immediately see an Alert on your screen:

![SilentSMS-Alert](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Alert.png)

Additionally, AIMSICD will show the following notification about the Interception in your notification bar:

![SilentSMS-Notification](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Notification.png)

##### Self-Test: Sending a Silent SMS (Type 0)

You can easily test if AIMSICD really can detect Silent SMS of Type 0 with the App [HushSMS](http://forum.xda-developers.com/showthread.php?t=1490484). Buy it [via PayPal](https://www.silentservices.de/products/android-hushsms/) and additionally install the [HushSMS Xposed Helper Module](https://silentservices.de/HushSMSExposedHelper.apk). Then open HushSMS and access the main screen as shown below:

![HushSMS](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS.png)

Now press the button "Send PING" and you will be taken to the screen below, through which you can select different types of PING SMS. Select the second option `Use Silent Ping (Type 0)` and send it to your own number. HushSMS will then send out a Silent SMS (but without the generation of a delivery receipt) to your own number. AIMSICD is not able to detect Silent SMS (Type 0) yet, but we're working hard on it.

![HushSMS-Type0](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS-Type0.png)

##### Class0 / Flash SMS / Popup SMS / Alert SMS

This type of SMS indicates that this message is to be displayed on the MS immediately and a message delivery report is to be sent back to the SC. The message does not have to be saved in the MS or on the SIM card (unless selected to do so by the mobile user). This type of SMS is not dangerous and hence we're not up to adding any detection mechanism for this type of SMS which is popping up on your screen anyway.