This is the "testers table" with the phones we're currently testing on and which one of us is using it. Table columns are: `Phone Model, Application Processor (AP) / Baseband Processor (BP), FW/ROM, AOS, API Version, *SELinux* Mode, Developer Name`

**Developers**: *Just copy the previous line and edit the relevant info.*

|           Phone Model           |   Application Processor, Baseband Processor   |               FW/ROM              |     AOS    | API |  SEL Mode  | DEV |
|:-------------------------------:|:---------------------------------------------:|:---------------------------------:|:----------:|:---:|:----------:|:-------:|
| Samsung Galaxy S4 Mini GT-I9195 |               MSM8930AB, [same]               |              *Stock*              |  JB 4.2.2  |  17 |  Enforced  |  E:V:A  |
|    Samsung Galaxy S2 GT-I9100   |                Exynos, XMM 6260               |              SlimKat              | KK 4.4.2b4 |  19 | Permissive |  E:V:A  |
|            HTC ONE M7           | 1.7 GHz quad-core Krait 300, Qualcomm MDM9x15 | [AOKP](http://aokp.co/) (latest)  |  KK 4.4.4  |  19 | Permissive | SecUpwN |
|       HTC Wildfire S A510e      |               ARM 1136EJ-S, ARM9              |                                   |            |     |            |  He3556 |
|          Wiko Darkmoon          |                     MT6582                    |              *Stock*              |  JB 4.2.2  |     | Permissive | andr3jx |
|                                 |                                               |                                   |            |     |            |         |




I Propose this...

| Manufacturer/Model    | Type-number | AP  | BP  | FW/ROM | AOS | API | SELmode | Dev |
|:--------------------- |:----------- | --- | --- |:------ |:--- | --- |:------- |:--- |
Samsung S2 | GT-I9100 | Exynos | XMM6260 | SlimKat | KK4.4.2b4 | 19 | Permissive | E:V:A
Samsung S4mini | GT-I9195 | ??? | ??? | *stock* | JB4.2.2 | 17 | Enforcing | E:V:A
HTC One | M7 | ??? | ??? | AOKP | KK4.4.4 | 19 | Permissive | SecUpwN
HTC Wildfire S | A510e | ??? | ??? | | | | He3556 |
Wiko Darkmoon | ? | MT6582 | SoC | *stock* | JB4.2.2 | | Permissive | andr3jx |

