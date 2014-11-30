This documentation is especially for developers who want to join our project and for everybody else who would like to know how AIMSICD detects IMSI-Catchers, silent SMS and other threats. Important Note: Due to its complexity, this is a work in progress.

***

**Basic Modules and I/O:**

![Program Modules](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/Program_Modules.png)

---

**Database Tables:**

![Database Tables](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/aimsicd_myCellInfo_ER_2.png)
* **DEFAULT_MCC_TABLE:** (Mobile Country Code): This table holds data to identify your service provider (carrier) and country.
* **CELL_TABLE:** Data collected by the phone when it is connected to a cell. (not from the table neighboring cells).
* **OPENCEllID_TABLE:** Downloaded DB from [OpenCellID](http://opencellid.org/).
* **LOCATION_TABLE:** Data collected by the phone. The location (Lat/Lng) of the phone and the Cell-ID it is connected to + timestamp.
* **SILENT_SMS_TABLE:** Protocol of incoming messages.

