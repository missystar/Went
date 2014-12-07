This is the **current** Development Status of our Android IMSI-Catcher Detector.
* :warning: [Development Roadmap](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#development-roadmap) with [ALPHA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#alpha-stage) & [BETA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#beta-stage) stage as well as [GOLDEN](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#golden-age) age.

---

### Already accomplished
Views (short explantation of the main views):
* [Main Screen](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Main-Screen): Information about Device, Network and SIM-Card
* [Cell Information](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Cell-Information): Relevant variables using public AOS API calls (LAC, CID, Signal Strength)
* [Database Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Database-Viewer): Data collected by the phone and from public DB of Cell Towers
* [Map Viewer](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Map-Viewer): Shows Cell-Towers from the public database that are in your area

Functions:
* Cell-Monitoring: Collects information about the cell towers you are/were  connected to and saves it in the local database
* [Cell Tracking](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Cell-Tracking): Tracks your position while you are connected to the cell-tower and saves it with cell data in the local database
* Download data from public cell-tower database (right now only from [OpenCellID](http://opencellid.org/))
* Position Tracking: Using the GPS-Sensor and Google Location Service

Detection:
* [Changing LAC](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/91): Check if the LAC of a Cell-ID is changing

---

### Working on right now
* Check Cell-ID’s collected by the phone against public Cell-Tower Database
* Neighboring Cell Info: [#100](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/100)
* AT-Command Processor:
Send AT-Commands to the Baseband Processor [#23](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/23)
* Detection of Silent SMS (Type-0): [#69](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)
* Specifications of code modularization (for development clarity)
* Restructuring of DB to allow for more Network variables (for development clarity)
* Separate DEbugging menu with much better way to create useable logcats: [#164](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/164)

---

### Prepared working packages (ready to be picked up)
* Detection of changing Signal Strength: Besides implementation, this needs lot’s of reasearch and testing, if this is a possible way for detection and how it works on different phones (meassurement of signal strength) ([more details](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/97))
* Switch from Google Location Servic (Google Play Service) to another API
* Implement the use of other public Cell-Tower Databases API‘s
