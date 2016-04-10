This documentation is especially meant for developers who want to join our project and for everybody else who would like to know more about the inner workings of `AIMSICD`. Due to its complexity, this is a work in progress.

# Index

* [Basic Modules and I/O](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#basic-modules-and-io)
* [Database Tables: (Current Behavior)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#database-tables-current-behavior)
* [DEFAULT_MCC_TABLE (Mobile Country Code)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#default_mcc_table-mobile-country-code)
* [CELL_TABLE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#cell_table)
* [LOCATION_TABLE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#location_table)
* [OPENCELLID_TABLE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#opencellid_table)
* [SILENT_SMS_TABLE](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#silent_sms_table)
* [Database Tables: (New Proposal)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#database-tables-new-proposal)
* [Accessing the Databases](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Technical-Overview#accessing-the-databases)

---

###**Basic Modules and I/O:**

![Program Modules](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Program_Modules.png)

---

###Database Tables:

One of our awesome developers is currently doing the heavy porting of our databases to [Realm](https://realm.io/).

![New Realm Database](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Database_myCellInfo_ER_4.png)

---

AIMSICD currently utilizes several tables in a single SQLite3 database in `aimsicd.db` to keep track 
of all the network changes and the downloaded Open Cell ID (OCID) data. When you're making a file 
backup of the AIMSICD database, you're actually saving the various tables into individual 
`aimsicd-<tablename>.CSV` files, which can be updated manually or externally.

All mentioned sqlite commands are properly documented on the [SQLite website](http://www.sqlite.org).

![Old Database Tables](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Database_myCellInfo_ER_3.png)

#### DEFAULT_MCC_TABLE (Mobile Country Code)
This table holds data to identify your service provider (carrier) and country.
#### CELL_TABLE
These are the *unique* BTS towers as collected by the phone, once it has connected to it (ignoring neighboring cells).
#### LOCATION_TABLE
These are the individual measurements as collected when in `Tracking Cell Details` mode. The location (Lat/Lng) of the phone and the Cell-ID it is connected to + timestamp.
#### OPENCELLID_TABLE
Downloaded DB from [OpenCellID](http://opencellid.org/).
#### SILENT_SMS_TABLE
Protocol of incoming messages.

---

#### Accessing the Databases

* From a PC

```
adb shell
su
sqlite3 /data/data/com.SecUpwN.AIMSICD/databases/aimsicd.db
```

* From a Terminal Emulator within Android
  * (Note: You may need to install sqlite3 binaries)

```
su
sqlite3 /data/data/com.SecUpwN.AIMSICD/databases/aimsicd.db
```

---

**To be updated** 

* **CELL_TABLE:** Data collected by the phone when it is connected to a cell. (not from the table neighboring cells).
* **LOCATION_TABLE:** These are the individual measurements as collected when in `Tracking Cell Details` mode. The location (Lat/Lng) of the phone and the Cell-ID it is connected to + timestamp.

***


**Other important details:** 

We display the Neighboring Cell information in two ways:   
1. through telephony manager methods which does not work on Samsung Devices   
2. a fallback is available through the methods developed by Alexey
(Data is saved in an Array not in an table)

***


**Further information about the actual status: [Development-Status](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status)**

