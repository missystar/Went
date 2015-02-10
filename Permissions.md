AIMSICD has tons of cool features, but you might be confused or worry why we need so many permissions. This page shall shed some light on this. Since our App needs to digg down deep into the baseband and read values that are normally not readable, the Android-IMSI-Catcher-Detector needs just about all variables, especially ROOT access for extended functions, but don't worry, it is not mandatory.

---

**Required Permissions**

```java
<uses-permission android:name="android.permission.ACCESS_SUPERUSER"/>
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
<uses-permission android:name="android.permission.ACCESS_COARSE_UPDATES"/>
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
<uses-permission android:name="android.permission.ACCESS_LOCATION_EXTRA_COMMANDS"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
<uses-permission android:name="android.permission.CHANGE_NETWORK_STATE" />
<uses-permission android:name="android.permission.INTERNET"/>
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE"/>
<uses-permission android:name="android.permission.READ_PHONE_STATE"/>
<uses-permission android:name="android.permission.READ_LOGS"/>
<uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED"/>
<uses-permission android:name="android.permission.RECEIVE_SMS"/>
<uses-permission android:name="android.permission.SYSTEM_ALERT_WINDOW"/>
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
<!-- NEW -->
<uses-permission android:name="android.permission.BLUETOOTH_PRIVILEGED"/>
<uses-permission android:name="android.permission.CHANGE_WIFI_STATE"/>
<uses-permission android:name="android.permission.KILL_BACKGROUND_PROCESSES"/>
<uses-permission android:name="android.permission.NFC"/>
<uses-permission android:name="android.permission.READ_CONTACTS"/>
<uses-permission android:name="android.permission.READ_SMS"/>
<uses-permission android:name="android.permission.RECEIVE_MMS"/>
<uses-permission android:name="android.permission.RECEIVE_WAP_PUSH"/>
<uses-permission android:name="android.permission.USE_SIP"/>
<uses-permission android:name="android.permission.VIBRATE"/>
<uses-permission android:name="android.permission.WAKE_LOCK"/>
<uses-permission android:name="android.permission.WRITE_SETTINGS"/>
<!-- SPECIAL PERMISSIONS TO BE ADDED AFTER THIS LINE. /> -->
<!-- To list all available (used) Android permissions on a device, use:
# `pm list permissions -g` -->
<!-- These are Android System (non 3rd party) Permissions -->
<uses-permission android:name="android.permission.CONTROL_LOCATION_UPDATES"/>
<uses-permission android:name="android.permission.DEVICE_POWER"/>
<uses-permission android:name="android.permission.DIAGNOSTIC"/>
<uses-permission android:name="android.permission.DUMP"/>
<uses-permission android:name="android.permission.FACTORY_TEST"/>
<uses-permission android:name="android.permission.HARDWARE_TEST"/>
<uses-permission android:name="android.permission.INJECT_EVENTS"/>
<uses-permission android:name="android.permission.INTERNAL_SYSTEM_WINDOW"/>
<uses-permission android:name="android.permission.LOCATION_HARDWARE"/>
<uses-permission android:name="android.permission.MODIFY_PHONE_STATE"/>
<uses-permission android:name="android.permission.SET_PROCESS_LIMIT"/>
<uses-permission android:name="android.permission.WRITE_APN_SETTINGS"/>
<uses-permission android:name="android.permission.WRITE_GSERVICES"/>
<uses-permission android:name="android.permission.WRITE_SECURE_SETTINGS"/>
<!-- possibly deprecated -->
<uses-permission android:name="android.permission.RECEIVE_EMERGENCY_BROADCAST"/>
<uses-permission android:name="android.permission.READ_NETWORK_USAGE_HISTORY"/>
<!-- These are OEM / Samsung Permissions -->
<uses-permission android:name="android.phone.receiveDetailedCallState"/>
<uses-permission android:name="com.android.permission.HANDOVER_STATUS"/>
<uses-permission android:name="com.sec.android.app.controlpanel.permission.PRIVATE"/>
<uses-permission android:name="com.sec.android.app.factorymode.permission.KEYSTRING"/>
<uses-permission android:name="com.sec.android.app.cm.permission.PERMISSION_MANAGEMENT"/>
<uses-permission android:name="com.sec.android.app.phoneutil.permission.KEYSTRING"/>
<uses-permission android:name="com.sec.android.app.servicemodeapp.permission.KEYSTRING"/>
<uses-permission android:name="com.sec.android.phone.permission.DATA_ROAMING_SETTINGS_ENHANCED"/>
<uses-permission android:name="com.sec.android.phone.permission.READ_CALL_SETTINGS"/>
<uses-permission android:name="com.sec.android.phone.permission.WRITE_CALL_SETTINGS"/>
<!-- uses-permission android:name="com.sec.factory.permission.ALLOWFTCLIENTCPOBIND"/>
<uses-permission android:name="com.sec.factory.permission.BT_ID_WRITE"/ -->
<uses-permission android:name="com.sec.factory.permission.KEYSTRING"/>
<uses-permission android:name="com.sec.modem.settings.permission.KEYSTRING"/>
<!-- uses-permission android:name="diagandroid.app.receiveDetailedApplicationState"/>
<uses-permission android:name="diagandroid.data.receivePDPContextState"/>
<uses-permission android:name="diagandroid.phone.receiveDetailedCallState"/ -->
<!-- May be needed (in the future) to access SIM related functions -->
<uses-permission android:name="org.simalliance.openmobileapi.SMARTCARD"/>
```

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