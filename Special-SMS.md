You already know the normal SMS you receive from friends and family once in a while. But in fact, there are other types of SMS which AIMSICD aims to detect and warn you about.

These are the results of our ongoing SMS detection tests:

| Phone         | Model      | AOS_VER | [Type-0](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/glossary-of-terms#silentstealth-sms) | [MWI](https://en.wikipedia.org/wiki/Message-waiting_indicator) | 
|:------------- |:---------- |:------- |:------ |:--- |
| HTC One       | M7         | LP5.1.1 |YES     | NO  | 

---

**Type-0 / Silent SMS / Stealth SMS / Ping SMS**

Law enforcement agencies are very often [see this German article](http://www.heise.de/newsticker/meldung/Zoll-BKA-und-Verfassungsschutz-verschickten-2010-ueber-440-000-stille-SMS-1394593.html) sending out so-called "Silent SMS" (also called Stealth SMS / Ping SMS), which is is a **[Type-0 SMS](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/glossary-of-terms#silentstealth-sms)**.

:exclamation: We just implemented detection of this type of message. [Help us improving it](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)!

If AIMSICD detects silent SMS (Type-0), you will see this alert on your screen:

![SilentSMS-Alert](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/SilentSMS-Alert.png)

Additionally, this notification will be shown in your notification bar:

![SilentSMS-Notification](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/SilentSMS-Notification.png)

---

##### Self-Test

You can easily test if AIMSICD really can detect Silent SMS of Type-0 with the app [HushSMS](http://forum.xda-developers.com/showthread.php?t=1490484). Buy it [via PayPal](https://www.silentservices.de/products/android-hushsms/), then open HushSMS and access its main screen:

![HushSMS](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/HushSMS.png)

Now press the button 'PING' and you will be taken to the screen below, through which you can select different types of PING SMS. Select the second option `Use Silent Ping (Type-0)` and send it to your own number. HushSMS will then send out a Silent SMS (but without the option of revealing the location of your phone) to your own number.

![HushSMS-Type0](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/HushSMS-Type0.png)

---

##### Add Detection

Our app has been designed in a way that enables you to easily add your own detection mechanism. Enter the `ADVANCED USER SETTINGS` via the `Preferences` and add your own detection string like `incoming msg. Mti 0 ProtocolID 0 DCS 0x04 class -1` to the menu `Detection Strings` and restart SMS detection.

If you found a new working string, please contact us for implementation.

---

**Flash SMS / Popup SMS / Alert SMS**

This type of SMS is per standard designed to immediately display in a pop-up window.
>A short message of class 0 indicates that this message is to be displayed on the MS immediately and a message delivery report is to be sent back to the SC. The message does not have to be saved in the MS or on the SIM card (unless selected to do so by the mobile user).

On most phones such messages cannot be saved. Those SMS are not dangerous. We're **NOT** going to add any detection mechanism for stuff which is popping up on your screen.