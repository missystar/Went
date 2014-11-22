This is the **current** Development Status of our Android IMSI-Catcher Detector.

## Already accomplished:
### Views (short explentation of the main views): 
* Information about Device, Network and SIM-Card, 
* Cell Information: Shows relevant variables using public AOS API calls. 
  (LAC, CID, Signal Strength)
* Database Viewer: Shows data collected by the phone and data from pulic database of Cell Towers
* Map-Viewer: Shows Cell-Towers from the public database that are in your area.


### Functions: 
* Cell-Monitoring: collecting information about the cell towers you are/were  connected to and save it in the local database
* Cell-Tracking: Tracks your position while you are connected to the cell-tower and save it with cell data in the local database
* Download data from public cell-tower database (right now only from Open CellID)
* Position Tracking: using the GPS-Sensor and Google Location Service


### Detection:
* Changing LAC: Check if the LAC of a Cell-ID is changing (more details: https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/91)


## Working on right now:
* Check Cell-ID’s collected by the phone agains public cell-tower db
* Neighbouring cell info: https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/100
* AT-Command Injector: Send AT-Commands to the Baseband Processor
* Detect Silent-SMS: 
* Specifications of code modularization (for development clarity)
* Restructuring of DB to allow for more Network variables (for development clarity)

## Prepared working packages (ready to be picked up) :
* Detection of changing Signal Strength: besides implementation, this needs lot’s of reasearch and testing, if this is a possible way for detection and how it works on different phones (meassurement of signal strength). More details: https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/97
* Switch from Google Location Servic (Google Play Service) to another API
* Implement the use of other public cell-tower databases API‘s


* [Development Roadmap](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#development-roadmap) with [ALPHA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#alpha-stage), [BETA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#beta-stage) and [GOLDEN](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector#golden-stage) stage.