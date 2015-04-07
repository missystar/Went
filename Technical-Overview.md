This documentation is especially for developers who want to join our project and for everybody else who would like to know how AIMSICD detects IMSI-Catchers, silent SMS and other threats. Important Note: Due to its complexity, this is a work in progress.

***

###**Basic Modules and I/O:**

![Program Modules](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Program_Modules.png)

---

###**Database Tables:** (Current Behavior)

![Database Tables](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Database_myCellInfo_ER_2.png)
* **DEFAULT_MCC_TABLE:** (Mobile Country Code): This table holds data to identify your service provider (carrier) and country.
* **CELL_TABLE:** These are the *unique* BTS towers as collected by the phone, once it has connected to it (ignoring neighboring cells).
* **LOCATION_TABLE:** These are the individual measurements as collected when in `Tracking Cell Details` mode. The location (Lat/Lng) of the phone and the Cell-ID it is connected to + timestamp.
* **OPENCELLID_TABLE:** Downloaded DB from [OpenCellID](http://opencellid.org/).
* **SILENT_SMS_TABLE:** Protocol of incoming messages.

---

**Database Tables:** (New Proposal)

![New Database Tables](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Database_myCellInfo_ER_3.png)



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


**Further information about the actual status and prepared working packages to be picked up by a developer:**
[Development-Status](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status)

