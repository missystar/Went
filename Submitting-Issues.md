# Trouble? Help us squashing bugz!

1. ALWAYS use the [latest WIP-Release](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/releases). **NO SUPPORT for older versions.**
2. If you use [Xprivacy](https://github.com/M66B/XPrivacy) read and understand [THIS](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Permissions) first! Give it another try after reading.
3. App still mocking around? Click [HERE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues) to open a new Issue. Name it appropriately.
4. On the top of the page, use the search bar to verify your Issue does not exist yet.
5. Describe your Issue as thoroughly as possible, let us reproduce it.
6. :skull: **NEVER** post your own unrelated stuff in existing Issues - it will piss us off!
7. Maintain your filed Issues! If you don't respond within 7 days, we will **CLOSE** it!

---

In all cases, you **MUST** include the following:

- **AIMSICD version (see the About-Tab within our App)**
- **Your exact FW specification (ROM, AOS API, etc.)**
- **Your exact HW specification (processor, model number, etc.)**
- **The output of getprop command to a Pastebin-Site (recommended: [PIE-Bin](https://defuse.ca/pastebin.htm))**
- :exclamation: **Logcat dump (press button `Send Error Log` in Navigation Drawer)**
- **Feel free to attach any other logs made by [CatLog](https://play.google.com/store/apps/details?id=com.nolanlawson.logcat) or [Logcat Extreme](https://play.google.com/store/apps/details?id=scd.lcex)**

---

**Are you a command line junkie?**

Then you can use the following commands that will:

 1. Create a log directory in: `/sdcard/aimsicd_log/`
 2. cd into that directory 
 3. Clear all the logcat's. 
 4. Run AIMSICD and wait for a key press to kill it.
 5. Save a full *logcat*, excluding that from *radio*, into the file `/sdcard/aimsicd_log/aimdump.log`.

Copy and paste the following to your android rooted shell.  
```bash
alias cdaim='mkdir /sdcard/aimsicd_log; cd /sdcard/aimsicd_log'
alias logclr='logcat -c -b main -b system -b radio -b events' 
alias logdmp='logcat -d -v threadtime -b main -b system -b events -f /sdcard/aimsicd_log/aimdump.log'
export DUMTXT="When bug occurs, press any key to kill app and dump logcat to file..."
alias aimrun='cdaim; logclr; am start -n com.SecUpwN.AIMSICD/.AIMSICD; read dummy?"${DUMTXT}"; am force-stop com.SecUpwN.AIMSICD; logdmp;'
```
To run it, just type: `aimrun`.
If you want to also supply *radio* logcat, add `-b radio` somewhere in the `logdmp` alias, but know that your GPS location and cell info may be included when you do that.

---

:exclamation: **SAFETY FIRST:** Remove your IMEI, IMSI and phone number from dumps you submit!

---

* Please **BE PATIENT**. Our developers have a real live, family, and jobs!
* If you like our project, feel free to submit code or find more developers. Thank you.