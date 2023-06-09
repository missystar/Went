:exclamation: **CAUTION: VERY ALPHA! ROOT IS REQUIRED!**

The AT Command Interface is now enabled thanks to the great work of [E3V3A](https://github.com/E3V3A) and [xLaMbChOpSx](https://github.com/xLaMbChOpSx). The current version of the AT Command Interface is accessible through the navigation drawer, but it will vanish into a special debugging menu in the future.

Root terminal methods are used to execute the AT Command. Therefore, this fragment will check for both ROOT (su binary) and BUSYBOX to confirm both are available on your device. If they are not available, the execution section of the fragment will NOT display.

If the initial setup works correctly the next step is trying to determine your RIL Serial Device through the system property `ril.libargs`. If this is successful then you are in business and the AT Command Interface system is available for you to test. This will probably NOT WORK on many devices (such as i9100) but it will provide details of the failure if available and display them to the screen but also write them to the file `error.txt` in the AIMSICD directory of your external storage (we are happy to receive these error reports to improve our App). Use the Timeout drop-down field to set a certain time for an AT Command response.

![AT Command Interface](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/SCREENSHOTS/AT-Command-Interface.png)