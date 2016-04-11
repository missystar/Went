This documentation is especially meant for developers who want to join our project and for everybody else who would like to know more about the inner workings of `AIMSICD`. Due to its complexity, this is a work in progress.

###Database Tables:

One of our awesome developers is currently doing the heavy porting of our databases to [Realm](https://realm.io/).

![New Realm Database](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/Database_myCellInfo_ER_4.png)

**Other important details:** 

We display the Neighboring Cell information in two ways:   
1. through telephony manager methods which does not work on Samsung Devices   
2. a fallback is available through the methods developed by Alexey
(Data is saved in an Array not in an table)

**Further information about the actual status: [Development-Status](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Development-Status)**
