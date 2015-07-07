You already know the normal SMS you receive from friends and family once in a while. But in fact, there are other types of SMS which AIMSICD aims to intercept and warn you about.

| Phone         | Model      | AOS_VER | Type-0 | MWI | 
|:------------- |:---------- |:------- |:------ |:--- |
| HTC One       | M7         | LP.1.1  |YES     | NO  | 

MWI = [Message Waiting Indicator](https://en.wikipedia.org/wiki/Message-waiting_indicator)

---

**Type0 / Silent SMS / Stealth SMS / Ping SMS**

Law enforcement agencies are very often [see this German article](http://www.heise.de/newsticker/meldung/Zoll-BKA-und-Verfassungsschutz-verschickten-2010-ueber-440-000-stille-SMS-1394593.html) sending out so-called "Silent SMS" (also called Stealth SMS / Ping SMS), which is is a **Type0 SMS**.

---

See our [Glossary of Terms](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/glossary-of-terms#silentstealth-sms) for a more detailed description.

---

Silent/Stealth SMS are specified in GSM 03.40 as follows:
>A short message type 0 indicates that the ME must acknowledge receipt of the short message but may discard its contents.

That means that those SMS do not show up on a display of a target device, nor trigger any acoustical signal when received. But when they are delivered they generate a delivery receipt and, most importantly, are recorded in a data retention database together with the location of a mobile phone which received it. There's no need for an IMSI-Catcher then. AIMSICD aims to detect and warn users of these.

:exclamation: We just implemented detection of this type of message. [Help us improving it](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)!

If AIMSICD intercepts silent SMS (Type 0), you will see this alert on your screen:

![SilentSMS-Alert](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/SilentSMS-Alert.png)

Additionally, this notification will be shown in your notification bar:

![SilentSMS-Notification](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/SilentSMS-Notification.png)

##### Self-Test: Sending a Silent SMS (Type 0)

You can easily test if AIMSICD really can detect Silent SMS of Type 0 with the app [HushSMS](http://forum.xda-developers.com/showthread.php?t=1490484). Buy it [via PayPal](https://www.silentservices.de/products/android-hushsms/), then open HushSMS and access its main screen:

![HushSMS](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/HushSMS.png)

Now press the button 'PING' and you will be taken to the screen below, through which you can select different types of PING SMS. Select the second option `Use Silent Ping (Type 0)` and send it to your own number. HushSMS will then send out a Silent SMS (but without the option of revealing the location of your phone) to your own number.

![HushSMS-Type0](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/HushSMS-Type0.png)

##### Add your own SMS type detection

Our app has been designed in a way that enables you to easily add your own detection mechanism. Enter the `ADVANCED USER SETTINGS` via the `Preferences` and add your own detection string like `incoming msg. Mti 0 ProtocolID 0 DCS 0x04 class -1` to the menu `Detection Strings` and restart SMS detection.

If you found a new working string, please contact us for implementation.

---

**Class0 / Flash SMS / Popup SMS / Alert SMS**

This type of SMS is per standard designed to immediately display in a pop-up window.
>A short message of class 0 indicates that this message is to be displayed on the MS immediately and a message delivery report is to be sent back to the SC. The message does not have to be saved in the MS or on the SIM card (unless selected to do so by the mobile user).

On most phones such messages cannot be saved. Those SMS are not dangerous. We're **NOT** adding any detection mechanism for stuff which is popping up on your screen.