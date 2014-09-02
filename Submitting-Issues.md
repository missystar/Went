# Trouble? Help us squashing bugz!

1. ALWAYS use the [latest WIP-Release](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/releases). **NO SUPPORT for older versions.**
2. If you use [Xprivacy](https://github.com/M66B/XPrivacy) read and understand [THIS](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Permissions) first! Give it another try after reading.
3. App still mocking around? Click [HERE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues) to open a new Issue. Name it appropriately.
4. On the top of the page, use the search bar to verify your Issue does not exist yet.
5. Describe your Issue as thoroughly as possible. You **MUST** include the following:

- **AIMSICD version (see the About-Tab within our App)**
- **Your exact FW specification (ROM, AOS API, etc.)**
- **Your exact HW specification (processor, model number, etc.)**
- **The output of getprop command to a Pastebin-Site (recommended: [PIE-Bin](https://defuse.ca/pastebin.htm))**
- **A logcat dump to Pastebin. We recommend to use [CatLog](https://play.google.com/store/apps/details?id=com.nolanlawson.logcat) or [Logcat Extreme](https://play.google.com/store/apps/details?id=scd.lcex)**

---
**Are you a command line junkie?**
Then you can use the following shell function to help you get only relevant logcat entries. 
Copy and paste the following to your terminal shell:
```
alias logrep='logcat -d -v time -b main -b system -b radio|grep -iE $@'
```
To use it just write: `logrep AIMSICD`, and you will only get stuff marked with AIMSICD.

---

:exclamation: **SAFETY FIRST:** Remove your IMEI, IMSI and phone number from dumps you submit!

---

* Please **BE PATIENT**. Our developers have a real live, family, and jobs!
* If you'd like our project, feel free to submit code or find more developers. Thank you.