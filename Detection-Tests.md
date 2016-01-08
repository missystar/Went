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

---

* `ID:2` - OsmocomBB BTS 'clones' an actual BTS with variable consistency and a legit BTS
* `ID:4` - OsmocomBB BTS doesn't allow TMSI allocation (red flag to tell if one is camped into a fake BTS)
* `ID:5` - OsmocomBB BTS allows choice of ciphering without droping/changing but doesn't allow A5/3 (not supported yet)
* `ID:6` - OsmocomBB BTS allows cipher downgrade
* `ID:7` - OsmocomBB BTS (tested with one BTS hence detectable as no neighbouring BTS are noted)
* `ID:18` - OsmocomBB BTS possible use of a jammer otherwise on its own OsmocomBB BTS cannot downgrade cell phone at will

---

![](https://cloud.githubusercontent.com/assets/8582348/11614451/88074c88-9c54-11e5-8e39-e436eaf7e8c3.png)
OsmocomBB + OpenBTS (with smqueue) running to create a fake BTS with some IMSIs captured.

---

![](https://cloud.githubusercontent.com/assets/8582348/11614397/f596bb28-9c52-11e5-896d-af045fa8f61e.jpg)

No neighboring cells are found as our BTS at the time of testing did not have this facilitated.

---

![](https://cloud.githubusercontent.com/assets/8582348/11614426/80182142-9c53-11e5-9d2b-b480a6e9a82d.jpg)

Our Phone details, when connected to the IMSI-Catcher.

---

![](https://cloud.githubusercontent.com/assets/8582348/11614450/88065972-9c54-11e5-95e1-e05551e3c638.jpg)

Sample of an SMS sent to the target phone from the IMSI-Catcher without causing alarm.
