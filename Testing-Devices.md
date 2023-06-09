This is the "testers table" with the phones we're currently testing on and which one of us is using it. Table columns are: `Manufacturer/Model, Type-Number, Application Processor (AP), Baseband Processor (BP), FW/ROM, AOS, API Version, *SELinux* Mode, Developer Name,  gsm.version.ril-impl`. The [SELinuxModeChanger](https://github.com/MrBIMC/SELinuxModeChanger) (get it [on F-Droid](https://f-droid.org/repository/browse/?fdid=com.mrbimc.selinux)) lets you change `SELmode`.

**Developers**: *Just copy the previous line and edit the relevant info.*

| Manufacturer/Model    | Type-Number | AP  | BP  | FW/ROM | AOS | API | SELmode | DEV | ril-impl |
|:--------------------- |:----------- | --- | --- |:------ |:--- | --- |:------- |:--- |:-------- |
HTC One | M7 | MSM8960 | *SoC* | AICP | MM6.0.1 | 23 | Permissive | SecUpwN | QRIL1.0
HTC Wildfire S | A510e | MSM7227T | *SoC* | CM10.1 | JB4.2.2 | 17 | *NE* | He3556 | ?
Huawei Ascend P1 | U9200 | OMAP4460 | XMM6260 | CM11 | KK4.4.4 | 19 | *NE* | tobykurien | XRIL1.0
Motorola Defy | MB525 | OMAP3610 | XMM? | | KK4.4.4 | 19 | | tobykurien | MRIL1.0 
Gigabyte GSmart | Arty A3 | MT6582 | *SoC* | *stock* | KK4.4.2 | 19 | Enforcing | E:V:A | MTG1.0 
Google Nexus 5 | "LG D821" | MSM8974 | *SoC* | *stock* | KK4.4.3 | 19 | Enforcing | Ueland | QRIL1.0
Google Nexus 5 | "LG D821" | ? | *SoC* | *stock* | M6.0 | 23 | ? | larsgrefer | ?
Google Nexus 7 | "3G-2012" | Tegra3 | XMM6260 | *stock* | KK4.4.4 | 19 | Enforcing| andr3jx | XRIL1.18
Samsung S2 | GT-I9100 | Exynos | XMM6260 | SlimKat | KK4.4.2b4 | 19 | Permissive | E:V:A | SIPCv2.0 
Samsung S2 | GT-I9100 | Exynos | XMM6260 | Carbon | KK4.4.4 | 19 | Permissive | xLaMbChOpSx | SIPCv2.0
Samsung S4 mini | GT-I9195 | MSM8930AB | *SoC* | *stock* | JB4.2.2 | 17 | Enforcing | E:V:A | QRIL1.0 
Samsung S4 mini | GT-I9195 | MSM8930AB | *SoC* | CM13 | M6.0.1 | 23 | Enforcing | mimi89999 | QRIL1.0 
Samsung G.Note | GT-N7000 | Exynos4210 | XMM6260 |  | KK4.4.4 | 19 |  | tobykurien | SIPCv2.0
Samsung Neo | GT-I5310 | BCM21654G | *SoC* | ? | JB4.1.2 | 16 | - | banjaxbanjo| BRCM1 
Sony Xperia J | ST26a | MSM7227A | *SoC* | ? | ? | ? | - | banjaxbanjo| ? 
Sony Xperia Z | C6603 | MSM8960 | *SoC* | *stock* | KK4.4.4 | 19 | Enforcing | xLaMbChOpSx | ?
Sony Xperia Z1 Compact |  | MSM8974 | *SoC* | *stock* | KK4.4.4 | 19 |  | scintill | QCRIL1.0
Wiko Darkmoon | ? | MT6582 | *SoC* | *stock* | JB4.2.2 | 17 | *NE*| andr3jx | ? 

Where:
 * *NE* = Not Enabled or Implemented
 * *SoC* = System on a Chip, which means that the Baseband Processor (BP) is integrated into the same chip as the Application Processor (AP)

| Notes | Description (gsm.version.ril-impl) | Manufacturer |
|:----- |:---------------------------------- |:------------ |
SIPCv2.0 | "Samsung RIL (IPC) v2.0" | Intel/Infinion
QRIL1.0 | "Qualcomm RIL 1.0" | Qualcomm
XRIL1.0 | "android infineon xgold-ril 1.0" | Intel/Infinion
XRIL1.18 | "android xgold-ril 1.18" | Intel/Infinion
MRIL1.0 | "android moto-ril 1.0" | ? 
MTG1.0 | "mtk gemini ril 1.0" | Mediatek
BRCM1 | "BRCM android bcm-ril-090728" | Broadcom

For an exhaustive list, look for your device [here](https://census.tsyrklevich.net/system_properties/gsm.version.ril-impl).

Commonly used serial devices for AT Command Processor access:

| Chip | AT access path | UART/cmdline |
|:---- |:-------------- |:------------ |
MT6582  | /dev/radio/atci1 | /dev/ttyMTo
MSM8930 | /dev/smd0 |
MSM8960 | /dev/smd0 |
MSM8974 |  |
OMAP3610 | /dev/ttyO | 