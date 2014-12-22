The Status Icons indicate several threat levels. 

As we're still working on implementing them all, we're still discussing them in issue 214, [here](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/214)

They are as follows:

**Short Explanations**

|  CODE  | ICON | THREAT-LEVEL |       SHORT EXPLANATION        |
|:------ |:----:|:------------ |:------------------------------ |
| Grey   | ![IDLE](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_idle.png)    | IDLE      | App is idling or loading. Stay tuned. |
| Green  | ![OK](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_ok.png)      | NORMAL       | No threats detected or found. |
| Yellow | ![MEDIUM](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_medium.png)  | MEDIUM       | Insecure Service Area: At least 1 new or unknown BTS, is in operation in this vicinity, or using encryption *<*A5/3  |
| Orange | ![HIGH](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_high.png)    | HIGH         | Hostile Service Actions Detected: An IMSI-Catcher is actively tracking users. |
| Red    | ![DANGER](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_danger.png)   | DANGEROUS    | Hostile Tracking Detected: An FBTS is actively tracking YOU. |
| Black  | ![SKULL](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_skull.png)    | RUN!         | Hostile Manipulation: Someone is trying to remotely manipulate your handset. |

---

**Detailed Explanations**


|  CODE  | ICON |              DETAILED EXPLANATION             |
|:------ |:----:|:--------------------------------------------- |
| Grey   | ![IDLE](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_idle.png)       | App is idling or loading. No protection and detection measures are enabled. Please open the [Navigation Drawer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer) and enable them in section `TRACKING`.    |
| Green  | ![OK](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_ok.png)         | No threats detected or found. Our App is constantly checking your network based upon the protection measures you've set in the [Navigation Drawer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer) and [Preferences](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer).   |
| Yellow | ![MEDIUM](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_medium.png)     | Hostile Service Area: One or more FBTS are in operation in this vicinity. ![Changing LAC](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/Changing_LAC.jpg) If AIMSICD shows up `Hostile Service Area: Changing LAC Detected!` in your notification bar, an IMSI-Catcher or fake Base Station may have been trying to send with more power than the original BTS which triggers your phone to connect to it. Detection is not complete yet. See [#91](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/91). |
| Orange | ![HIGH](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_high.png)       | Hostile Service Actions Detected: An FBTS is actively tracking users. Scanning takes place in this area. You should leave this place as soon as possible!                               |
| Red    | ![DANGER](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_danger.png)     | Hostile Tracking Detected: An FBTS is actively tracking YOU. The IMSI of your phone has been catched and an IMSI-Catcher is following you around!                         |
| Black  | ![SKULL](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_skull.png)      | Hostile Manipulation: Someone is trying to remotely manipulate your handset. If you **really should** throw that device away and change your phone somewhere far away (don't carry your old phone to the changing place). Use a new (preferably anonymous) SIM card, change calling behavior and warn your friends - not by calling them, but by talking to them in real life!  |
