The Status Icons indicate several threat levels. 

As we're still working on implementing them all, we're still discussing them in [Issue 214](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/214)!

They are as follows:

**Short Explanations**

|  CODE  | ICON | THREAT-LEVEL |       SHORT EXPLANATION        |
|:------ |:----:|:------------ |:------------------------------ |
| Grey   | ![IDLE](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_idle.png)    | IDLE      | App is idling or loading. Stay tuned. |
| Green  | ![OK](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_ok.png)      | NORMAL       | No threats detected or found. Your network is using A5/3 or better. |
| Yellow | ![MEDIUM](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_medium.png)  | MEDIUM       | _Insecure Service Area_: At least 1 new or unknown BTS is in operation in this vicinity, or using an encryption **<** A5/3. |
| Orange | ![HIGH](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_high.png)    | HIGH         | _Hostile Service Actions_ Detected: An IMSI-Catcher is actively tracking users. |
| Red    | ![DANGER](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_danger.png)   | DANGEROUS    | _Hostile Tracking Detected_: An FBTS is actively tracking YOU. Leave this place! |
| Black  | ![SKULL](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_skull.png)    | RUN!         | _Hostile Manipulation_: Someone is trying to remotely manipulate your handset, YOU are the TARGET! |

---

**Detailed Explanations**


|  CODE  | ICON |              DETAILED EXPLANATION             |
|:------ |:----:|:--------------------------------------------- |
| Grey   | ![IDLE](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_idle.png)       | App is idling or loading. No protection and detection measures are enabled. Please open the [Navigation Drawer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer) and enable them in section `TRACKING`.    |
| Green  | ![OK](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_ok.png)         | No threats detected or found. Our App is constantly checking your network based upon the protection measures you've set in the [Navigation Drawer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer) and [Preferences](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Navigation-Drawer).   |
| Yellow | ![MEDIUM](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_medium.png)     | _Insecure Service Area_: At least 1 new or unknown BTS is in operation in this vicinity, or using an insecure (broken) encryption algorithm lower than A5/3  [NEED FIX!] Expect that any phone calls/SMS made in this area can be intercepted and recorded. You better leave this place now. |
| Orange | ![HIGH](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_high.png)       | _Hostile Service Actions_ Detected: An An IMSI-Catcher (IMSIC) or fake BTS (FBTS) is actively tracking users. Active scanning takes place in this area. You should avoid this place, especially if there are political unrest. Take out your battery or [kill your phone](http://killyourphone.com/)! |
| Red    | ![DANGER](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_danger.png)     | _Hostile Tracking Detected_: An FBTS or IMSIC is actively tracking YOU and preventing your phone from connecting through your normal encrypted mobile provider. If you're in danger or repercussions, destroy your phone + SIM and report it as recently stolen. |
| Black  | ![SKULL](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/master/app/src/main/res/drawable-hdpi/sense_skull.png)      | _Hostile Manipulation_: Someone is trying to remotely manipulate your handset. **Destroy** (or sell) your phone and get a new one somewhere far away (don't carry your old phone to the changing place). Use a new (preferably anonymous) SIM card, change calling behavior and warn your friends - not by calling them, but by talking to them in real life!  |
