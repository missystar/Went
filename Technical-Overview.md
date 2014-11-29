This documentation is especially for developers who wants to join the project and for everybody else who wants to know how AIMSICD detects IMSI-Catchers, silent SMS and other threats. 

***

**Basic Modules and I/O:**

![Program Modules](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/Program_Modules.png)

***

**Database Tables:**
![Database Tables](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/aimsicd_myCellInfo_ER_2.png)
**DEFAULT_MCC_TABLE:** (Mobile Country Code): This table holds data to identify your service provider (carrier) and country.
**CELL_TABLE:** Data is collected by the Phone when it is connected to a Cell. (not from the table neighboring cells) 
**OPENCEllID_TABLE:** Downloaded DB from OpenCellID.
**LOCATION_TABLE:** Data is collected by the Phone. The location (lat/lng) of the phone and the Cell-ID it is connected to + timestamp.
**SILENT_SMS_TABLE:** Protocol of incoming messages