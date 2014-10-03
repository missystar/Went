This is the "testers table" with the phones we're currently testing on and which one of us is using it. Table columns are: `Manufacturer/Model, Type-Number, Application Processor (AP), Baseband Processor (BP), FW/ROM, AOS, API Version, *SELinux* Mode, Developer Name,  gsm.version.ril-impl`

**Developers**: *Just copy the previous line and edit the relevant info.*

| Manufacturer/Model    | Type-Number | AP  | BP  | FW/ROM | AOS | API | SELmode | DEV | ril-impl |
|:--------------------- |:----------- | --- | --- |:------ |:--- | --- |:------- |:--- |:-------- |
Samsung S2 | GT-I9100 | Exynos | XMM6260 | SlimKat | KK4.4.2b4 | 19 | Permissive | E:V:A | Samsung RIL(IPC) v2.0 |
Samsung S2 | GT-I9100 | Exynos | XMM6260 | Carbon | KK4.4.4 | 19 | Permissive | xLaMbChOpSx | 
Samsung S4 mini | GT-I9195 | MSM8930AB | *SoC* | *stock* | JB4.2.2 | 17 | Enforcing | E:V:A | 
Sony Xperia Z | C6603 | MSM8960 | *SoC* | *stock* | KK4.4.4 | 19 | Enforcing | xLaMbChOpSx | 
HTC One | M7 | MSM8960 | *SoC* | AOKP | KK4.4.4 | 19 | Permissive | SecUpwN | 
HTC Wildfire S | A510e | MSM7227T | *SoC* | CM10.1 | JB4.2.2 | 17 | *NE* | He3556 | 
Wiko Darkmoon | ? | MT6582 | *SoC* | *stock* | JB4.2.2 | 17 | *NE*| andr3jx | 
Huawei Ascend P1 | U9200 | OMAP4460 | XMM6260 | CM11 | KK4.4.4 | 19 | *NE* | tobykurien | 
Nexus 7 3G (2012) | ? | Tegra3 | XMM6260 | *stock* | KK4.4.4 | 19 | Enforcing| andr3jx | 


"NE" = Not Enabled/Implemented

"SoC" = System on a Chip, which means that the BP is integrated into the same chip as the AP