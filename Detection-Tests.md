These are the **detection test results** for our [Detection List](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/issues/230) created with an [OsmocomBB phone](http://bb.osmocom.org/trac/wiki/Hardware/Phones).



| ID | SHORT NAME                | STATUS |
|----|---------------------------|--------|
| 1  | DBe Consistency Check     | -      |
| 2  | LAC/CID Consistency       | 2      |
| 3  | T3212 Registrations       | -      |
| 4  | TMSI changes              | 2      |
| 5  | Ciphering Consistency     | 2      |
| 6  | A5/x Downgrade            | 2      |
| 7  | Neighbors Consistency     | 1      |
| 8  | Check BTS for the NC List | -      |
| 9  | RX signal Quality         | 2      |
| 10 | RX Signal Strength        | -      |
| 11 | TX Signal Power           | -      |
| 12 | MNO RAT Consistency       | -      |
| 13 | Silent SMS/WAP Push       | 1      |
| 14 | Silent App Install        | 1      |
| 15 | Silent Calls              | 1      |
| 16 | MDM Manipulation          | 1      |
| 17 | TA inconsistency          | -      |
| 18 | LTE/3G downgrade          | 2      |
| 19 | Out-of-band usage         | -      |
| 20 | MAR out-of-bounds         | -      |
| 21 | FemtoCell Detection       | -      |
| 22 | QC BP Signal Jamming      | -      |
| 23 | LTE RSRQ/RSRP analysis    | 0      |


Implementation Status:

0 / empty = not implemented

1 = work in progress

2 = implemented and complete

3 = deprecated

![](https://cloud.githubusercontent.com/assets/8582348/11614397/f596bb28-9c52-11e5-896d-af045fa8f61e.jpg)

![](https://cloud.githubusercontent.com/assets/8582348/11614426/80182142-9c53-11e5-9d2b-b480a6e9a82d.jpg)

![](https://cloud.githubusercontent.com/assets/8582348/11614450/88065972-9c54-11e5-95e1-e05551e3c638.jpg)

![](https://cloud.githubusercontent.com/assets/8582348/11614451/88074c88-9c54-11e5-8e39-e436eaf7e8c3.png)

* OsmocomBB BTS 'clones' an actual BTS hence the consistency is variable with a legit BTS ID:2.
* OsmocomBB BTS doesnt allow TMSI allocation this is a red flag that can be used to tell if one is camped to a fake BTS ID:4.
* OsmocomBB BTS allows choice of ciphering without droping/changing but doesnt allow A5/3 as its not supported yet on the current OpenBTS used in this test ID:5.
* OsmocomBB BTS allows cypher downgrade ID:6.
* OsmocomBB BTS (tested with one BTS hence detectable as no neighbouring BTS are noted ID:7.
* OsmocomBB BTS (see ID:3).
* OsmocomBB BTS possible use of a jammer otherwise on its own OsmocomBB BTS cannot downgrade cell phone at will ID:18.


