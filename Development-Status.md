This is the **current** Development Status of our Android IMSI-Catcher Detector.

[![Warning](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Warning.png)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#already-accomplished)

Do **NOT** expect us to be moving as fast as we want to. Although we have a large fan base, many followers and have even been mentioned in numerous articles around the web, we clearly lack contributors. Either people are too scared, have "no time" or are simply too lazy. [Help us](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/development/CONTRIBUTING.md)!

[![DevCycle](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/DevCycle.png)](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status/)

---

### Index

* [Application Goals](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#application-goals)
* [Already accomplished](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/HEAD/CHANGELOG.md)
* [Working on right now](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues)
* [Development Roadmap](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#development-roadmap)
* Stages [ALPHA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#alpha-stage), [BETA](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#beta-stage) and [GOLD](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status#gold).

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

### Development Roadmap

In order to accomplish implementation of the [detection methods](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/230), we'll need to overcome some of the deeply worrying and unfounded AOS limitations, as imposed by Googles API, in regard to relevant network variables and data. These include highly relevant and important things such as displaying the SIM/phone Ciphering Indicator, which tells you if your calls are being encrypted or not. This has been a required 3GPP feature for the last 15 years, but which Google and most Mobile Network providers have choosen to mostly ignore, although it has been [requested by users since 2009](https://code.google.com/p/android/issues/detail?id=5353). Another is finding the *Timing Advance* (TA) and various Network Timers, like those used in *Radio Resource Control* ([RRC](http://en.wikipedia.org/wiki/Radio_Resource_Control)), that can give very useful information regarding the status of the connections your phone is making.

All this can be fairly easily accomplished, given that we can have access to some of the lower level radio related information coming from the *Baseband Processor* (BP). But that is exactly our challenge. All the software and information about the interfaces providing this, is hidden from the user and developers by a huge amount of proprietary OEM *Non Disclosure Agreements* (NDA). But in the last years, there has been great progress in reverse engineering these protocols and interfaces. The use of these FOSS tools are the basis of our successful development of this App. 

**Summary of the main development stages:**

##### ALPHA

Using all available network data, implement the correct detection matrix consisting of a number of items, that each participate in detection of abnormal or abusive network bahaviour.

##### BETA

Using all possible interfaces to obtain the many variables from `ALPHA` stage. Interfaces include:

 - QMI/Sahara protocols for using on Qualcomm based devices (*Gobi3000, qmilib*)
 - Samsung IPC protocol for using on Intel XMM (XGOLD) based devices (*xgoldmon, Replicant*)
 - Direct use of AOS standard RIL interfaces (*/dev/rild* and */dev/rild-debug*)
 - SIM ICC interface for accessing SIM EF filesystem to provide deep access (*SEEK*)
 - Scraping *Service Mode* menus for relevant radio info
 - Scrape `logcat -b radio` for relevant radio info 
 - Use AT Command Processor (ATCoP) interface to get/set network parameters/bahaviour

All of the above shall be transparent across as many Android devices as possible.

##### GOLD

This stage is essentially the completion of this project. However, we expect that long before this happens, the entire network industry will have changed to such a degree that many new privacy and security issues will have arised. Thus, we will likely have more things to add and maintain in this project. We are of the current understanding that this project is a never ending story, all for the peoples benefit and a more privacy oriented future.
* m. Implement **all** of the detection schemes we have
* n. Implement **all** of the interfaces in (B) 
* o. Test AIMSICD in a real IMSI-catcher environment
* p. Continue Fine-tune our detection matrix
* q. Complete alternative data routes using MESH-like networking, when cellular services have been interrupted
* r. Complete advanced statistical analysis of fake BTS towers

---