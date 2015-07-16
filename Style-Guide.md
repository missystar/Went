This is our Style Guide to reflect our Corporate Design within our App.

### Index of Contents

* [Logo](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#logo)
* [Fonts](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#fonts)
* [Icons](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#icons)
* [Forms](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#forms)
* [Colors](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#colors)
* [Layout](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#layout)
* [Coding](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#coding)
* [Formats](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#formats)
* [Elements](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#elements)
* [Navigation](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#navigation)
* [Illustrations](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/wiki/Style-Guide#illustrations)

**Mindset:** Simple and intuitive, data is more important than looks.

---

#### Logo

![AIMSICD-Banner](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/PROMOTION/AIMSICD-Banner_Small.png)

Our main App Icon is the red Status Icon indicating threat status `DANGER`. You can either take it directly from our Apps `drawable-xxxhdpi` folder by clicking [here](https://raw.githubusercontent.com/SecUpwN/Android-IMSI-Catcher-Detector/HEAD/app/src/main/res/drawable-xxxhdpi/sense_danger.png), or by manually extracting it from our [Banner SVG](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/PROMOTION/AIMSICD-Banner.svg) or [Status Icons SVG](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/PROMOTION/AIMSICD-Status-Icons.svg) file.

---

#### Fonts

No final decision yet. We prefer open source fonts on GitHub. Some inspiration:

* [Calligraphy](https://github.com/chrisjenx/Calligraphy)
* [Proxima Nova](http://www.myfonts.com/fonts/marksimonson/proxima-nova/) (not free, used by Spotify)
* [Museo Slab 500](https://www.myfonts.com/fonts/exljbris/museo-slab/500/) (not free)

Want to identify your favorite font? Use [WhatTheFont](http://www.myfonts.com/WhatTheFont/)!

---

#### Icons

No final decision on in-app icons yet. Some inspiration:

* [Material Design Icons](https://github.com/google/material-design-icons/)
* [Iconmonstr](http://iconmonstr.com/)
* [Android Icons](http://www.androidicons.com/)

---

#### Forms

* No rounded corners
* Round Icons without outline (except Status Icons)
* Square Buttons if text is used
* Round Buttons if Icons or signs are used

![Forms](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/Forms.png)

---

#### Colors

![Device_Details](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/Device_Details.png)

| COLOR |  #HEX   |                 DESCRIPTION                   |
|:-----:|:-------:|:---------------------------------------------:|
| ![111111](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/111111.png)       | #111111 | Background color: Screen and Navigation  | 
| ![333333](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/333333.png)      | #333333 | Outline of boxes, background of box header, background of Navigation Drawer, form fields (text input, select box)  |
| ![ffec5a](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/ffec5a.png)      | #ffec5a | Akzent Color, text of box headlines, buttons  |
| ![929292](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/929292.png)      | #929292 | Describing text of values, "unimportant" text (for better overview) |    
| ![f9f9f9](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/f9f9f9.png)      | #f9f9f9 | "Important" values (good readability) |
| ![ab2424](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/ab2424.png)      | #ab2424 | Map Marker (single tower), text color for alerts of all kind (or as box background color) |
| ![35b838](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/35b838.png)      | #35b838 | Map Marker (more towers) |             
| ![2668a0](https://spideroak.com/share/IFEU2U2JINCA/GitHub/home/SecUpwN/SpiderOak/DOCUMENTATION/StyleGuide/2668a0.png)      | #2668a0 | Neutral color, use for small objects (own position in the map) |

---

#### Layout

* Careful use of space, don't leave great spaces

---

#### Coding

As much as we enjoy your contributions, please keep a high code-quality!

* Follow the [Android Code Style Guidelines](https://source.android.com/source/code-style.html)
* Make use of the [Android Best Practices](https://github.com/futurice/android-best-practices)
* Also respect the [Google Java Style](https://google.github.io/styleguide/javaguide.html), but:

>* No column limit to 100 char. (As we all know, our screens are 1 kilometer wide and about 2 centimeters high, so why should we read code 2 cm wide and have to scroll downwards paging through 1 kilometer?)
>* No line wrapping. Nobody likes line-wrapping, unless there's a bunch of consecutive objects wit the same name/structure that can be nicely aligned.
>* Skip point `4.6.3 - Horizontal alignment`. E:V:A loves horizontal alignment, and as long as we use spaces and not tabs, its perfectly great for readability.
>* Another good thing to know: `Class and member modifiers, when present, appear in the order recommended by the Java Language Specification:`
```JAVA
public protected private abstract static final transient volatile synchronized native strictfp
```

---

#### Formats

* Flat Design (no shadows, no bevel, no shining edges)
* Rectangular prisms (if possible), 100% width for boxes and tables 

---

#### Elements

* Thin lines color `#333333` between text blocks and in the Navigation Drawer

---

#### Navigation

Easy, intuitive and self-explaining. Preferably giving a unique look and feel to our app.

* [Awesome Android UI/UX Libraries](https://github.com/wasabeef/awesome-android-ui)

---

#### Illustrations

* 1 Color Icons, flat and minimalistic

---