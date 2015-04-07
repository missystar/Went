This is the **current** Development Status of our Android IMSI-Catcher Detector.

[![DevCycle](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/DevCycle.png)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status/)

:warning: Do **NOT** expect us to be moving as fast as we want to. Although we have a large fan base, many followers and have even been mentioned in numerous articles around the web, we clearly lack contributors. Either people are too scared, have "no time" or are simply too lazy. If **YOU** consider yourself to be different, prove it and [contribute](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/development/CONTRIBUTING.md)!

---

### Index

* [Application Goals](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#application-goals)
* [Already accomplished](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#already-accomplished)
* [Working on right now](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#working-on-right-now)
* [Prepared working packages](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#prepared-working-packages-ready-to-be-picked-up)
* [Development Roadmap](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#development-roadmap)
* Stages: [ALPHA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#alpha-stage), [BETA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#beta-stage) and [GOLDEN](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#golden-age) age.

---

### Application Goals

Below goals are aimed to be reached with our [detection list](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/230):

* Detect IMSI based device location tracking
* Detect and prevent the use of false BTS towers used for illegal interception
* Detect and prevent the use of broken ciphering algorithms (A5/1) during calls
* Detect and prevent remote hidden application installation
* Detect and prevent remote hidden SMS-based SIM attacks
* Provide counter measures against tracking
* Prevent leakage of sensitive GPS data
* Provide swarm-wise-decision-based cellular service interruption
* Provide secure wifi/wimax alternative data routes through MESH-like networking
* Aims to be recommended and added to the [Guardian Project's list of secure Apps](https://guardianproject.info/apps)
* Aims to be recommended by the [SSD Project of the Electronic Frontier Foundation](https://ssd.eff.org/)
* Aims to be recommended by [Privacy International](https://www.privacyinternational.org/) (and like-minded organizations)

---

### Already accomplished
Views (short explanation of the main views):
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
* Check Cell-ID’s collected by the phone against public Cell-Tower Database.
* Check for "Changing LAC" of each Cell-ID that is collected by by the phone.  

---

### Working on right now
* Neighboring Cell Info: [#100](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/100)
* AT-Command Processor:
Send AT-Commands to the Baseband Processor [#23](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/23)
* Detection of Silent SMS (Type-0): [#69](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/69)
* Specifications of code modularization (for development clarity)
* Restructuring of DB to allow for more Network variables (for development clarity)
* Separate Debugging menu with much better way to create useable logcats: [#164](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/164)
* Detection of changing Signal Strength: Besides implementation, this needs lot’s of research and testing, if this is a possible way for detection and how it works on different phones (measurement of signal strength) ([more details](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/97))
* Check BTS for the NC List [#264](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/264)

---

### Prepared working packages (ready to be picked up)

* Implement the use of other public Cell-Tower Databases API‘s
* We are preparing further working packages of this [Detection List](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/230) As soon as they are ready, we will add them to this list.

---

### Development Roadmap

In order to accomplish implementation of the [detection methods](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/230), we'll need to overcome some of the deeply worrying and unfounded AOS limitations, as imposed by Googles API, in regard to relevant network variables and data. These include highly relevant and important things such as displaying the SIM/phone Ciphering Indicator, which tells you if your calls are being encrypted or not. This has been a required 3GPP feature for the last 15 years, but which Google and most Mobile Network providers have choosen to mostly ignore, although it has been [requested by users since 2009](https://code.google.com/p/android/issues/detail?id=5353). Another is finding the *Timing Advance* (TA) and various Network Timers, like those used in *Radio Resource Control* ([RRC](http://en.wikipedia.org/wiki/Radio_Resource_Control)), that can give very useful information regarding the status of the connections your phone is making.

All this can be fairly easily accomplished, given that we can have access to some of the lower level radio related information coming from the *Baseband Processor* (BP). But that is exactly our challenge. All the software and information about the interfaces providing this, is hidden from the user and developers by a huge amount of proprietary OEM *Non Disclosure Agreements* (NDA). But in the last years, there has been great progress in reverse enginering these protocols and interfaces. The use of these open source tools are the basis of our successful development of this App. 

**Summary of the main development stages:**

**A.** Using all available network data, implement the correct detection matrix consisting of a number of items, that each participate in detection of abnormal or abusive network bahaviour. This is the application *[Beta](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/README.md#beta-stage)* stage. 

**B.** Using all possible interfaces to obtain the many variables in (A). These interfaces include:
 - QMI/Sahara protocols for using on Qualcomm based devices (*Gobi3000, qmilib*)
 - Samsung IPC protocol for using on Intel XMM (XGOLD) based devices (*xgoldmon, Replicant*)
 - Direct use of AOS standard RIL interfaces (*/dev/rild* and */dev/rild-debug*)
 - SIM ICC interface for accessing SIM EF filesystem to provide deep access (*SEEK*)
 - Scraping *Service Mode* menus for relevant radio info
 - Scrape `logcat -b radio` for relevant radio info 
 - Use AT Command Processor (ATCoP) interface to get/set network parameters/bahaviour

**C.** Make (A) and (B) transparent across as many Android devices as possible.

##### ALPHA stage:

Make a baseline App that contains the basic functionality for collecting and presenting all available network variables and the detection results.

* a. Collects relevant RF related variables using public AOS API calls. (LAC, CID, TA etc)
* b. Collects detailed BTS information from a pulic database such as *OpenCellID* or *Mozilla Location Services*
* c. Save everything in our SQLite database
* d. Detect hidden/silent (Type-0) SMS's
* e. Detect hidden App installations (Googles INSTALL/REMOVE_ASSET)

##### BETA stage:

Improve ALPHA for leveraging and tune our detection matrix/algorithm.
* f. Implement **any** of the detection schemes we have
* g. Implement **any** of the interfaces in (**B**) 
* h. Test AIMSICD in a real IMSI-catcher environment 
* i. Fine-tune our detection matrix
* j. Implement our first counter interception measures
* k. Planning alternative data routes through MESH-like networking, when cellular services have been interrupted
* l. Planning swarm-wise decision-based cellular service analysis (advanced BTS statistics)

##### GOLDEN age:

This stage is essentially the completion of this project. However, we expect that long before this happens, the entire network industry will have changed to such a degree that many new privacy and security issues will have arised. Thus, we will likely have more things to add and maintain in this project. We are of the current understanding that this project is a never ending story, all for the peoples benefit and a more privacy oriented future.
* m. Implement **all** of the detection schemes we have
* n. Implement **all** of the interfaces in (B) 
* o. Test AIMSICD in a real IMSI-catcher environment
* p. Continue Fine-tune our detection matrix
* q. Complete alternative data routes using MESH-like networking, when cellular services have been interrupted
* r. Complete advanced statistical analysis of fake BTS towers
