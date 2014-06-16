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

* [Silent SMS Interception](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/User-Guide#silent-sms-interception)

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

If you want to track Cell Data, enabling Location Services is required. If disabled, AIMSICD will look like this in your notification bar:

![Tracking_Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Disabled.png)

Furthermore, you will be prompted to enable Location Services:

![LocationServices-Disabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/LocationServices-Disabled.png)

When Location Services have been enabled, AIMSICD will look like this in the notification bar:

![Tracking_Enabled](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Tracking_Enabled.png)

---

# About AIMSICD

This tab provides a convenient overview with several links to important information, especially the version number of your installed AIMSICD (which you should include in every bug report). All links are self-explanatory.

![About AIMSICD](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/About_AIMSICD.png)

# Options Menu

This menu can be accessed through pressing on the three dots in the upper right corner of AIMSICD. You can either chose to navigate to the Preferences, the Database Viewer, backup the Database, restore the Database, update OpenCellID Data or Quit the App.

![Options Menu](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Options_Menu.png)

# Preferences

Here you can fine-tune our App. The preferences are self-explanatory. On the very bottom you can also select the style of the Icons that are displayed by AIMSICD - these can be either a style of "Flat", "Sense" or "White".

![Preferences](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/Preferences.png)

---

# Silent SMS Interception

Law enforcement agencies are very often sending out so-called "silent SMS" ([see this German article](http://www.heise.de/newsticker/meldung/Zoll-BKA-und-Verfassungsschutz-verschickten-2010-ueber-440-000-stille-SMS-1394593.html)) which do not show up on a display of a target device, nor trigger any acoustical signal when received. But when they are delivered they generate a delivery receipt and, most importantly, are recorded in a data retention database together with the location of a mobile phone which received it. There's no need for an IMSI-Catcher then. Reliable detection of silent SMS will be trivial to the usefulness of AIMSICD and is still being worked on.

If AIMSICD intercepts a Silent SMS, you will immediately see an Alert on your screen:

![SilentSMS-Alert](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Alert.png)

Additionally, AIMSICD will show the following notification about the Interception in your notification bar:

![SilentSMS-Notification](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/SilentSMS-Notification.png)

##### Self-Test through using HushSMS

If you would like to test how AIMSICD reacts on receival of a Silent SMS, install the latest version of [HushSMS](http://forum.xda-developers.com/showthread.php?t=1490484) as well as the [HushSMS Xposed Helper Module](https://silentservices.de/HushSMSExposedHelper.apk) and access the main screen of HushSMS as shown below:

![HushSMS](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS.png)

In the upper right corner of HushSMS, click the button named "Send Class 0" and you will see the screen shown below. Type in your own phone number as well as any message you would like and click on "Send Class 0". AIMSICD will instantly react accordingly.

![HushSMS-Class0](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/SCREENSHOTS/HushSMS-Class0.png)