Welcome to the place of questions asked a million times! Get your answer here. Again. :smile_cat: 

**Q: Is this a fully functional project or a prototype?**

A: This is a work in progress (WIP) and that is exactly the reason why we are fully open source. It is a difficult task to reach our desired goals. If it was fully functional already, we would probably not have invited you to develop with us. But that does not mean you cannot already test it - grab the [latest WIP-Release](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/releases) or compile it yourself.

**Q: Who are you guys?**

A: Contrary to some of our competitor opinion, we're **not** *M3g4G4lacticEl33tHAxor5*, we're just a collection of ordinary and slightly above average tech savvy concerned citizens, who have a strong belief that individual privacy should be a basic human right and a personal choice, and not something your government can suddenly dispose of at any whim of an impulse. That is why we stand up and do something about it.

**Q: Why are you anonymous?**

A: Not all of us are anonymous, but we respect the fact that some of us would like to remain that way. This answer is probably slightly different for all of us. For example, E:V:A thinks:

Personally I have no problem of going public on this. I don't think anyone would come after me, at least not for something bad, but probably more to ask me to work for 'them'. However, there are mainly 3 reasons I choose not to.

1. I have a company in a completely different field, and I do not wish to associate my hobby with that company. 
2. I'm also doing it out of principle. The principle that people should be able to stay anonymous without repercussions. Privacy should be the norm, not the other way around. 
3. The project is still in **ALPHA stage**, so it would be wrong to start making public presentations for something that only partially works on a few selected devices. 


**Q: What role do you want me to play ?**

A: That solely depends on your capabilities, time and mindset. In an ideal world, you'd be primarily solving the Issues on our GitHub, contribute code through pull requests, test our App thoroughly and tell your friends. But honestly speaking, noone wants to force you doing anything. You can also just lurk around and complain that nothing is working.

**Q: In what way will you compensate the work?**

A: Well, great question. First of all, we are a fully open-source project and as such, everyone is free to contribute whatever they feel willing to. We have set up a way of collecting anonymous donations via DarkCoin and upon great contributions our team eventually sends out what's in the bowl to the corresponding developer. Given the fact that our project is open-source and to certain folks not as addicting as Candy Crush (ok, we admit it, we are obsessed with our project and deleted Candy Crush) the bowl is not filling itself with as much money as we'd like to hand out. But if you consider getting a little fame through being mentioned in our [CREDITS](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/CREDITS) to be an adequate "compensation", we definitely pay that one. We know that nobody is doing shit for free, but with a glimpse of hope, we try to make this value-based world out there may feel warm and fuzzy about our carefully crafted, and with much love coded fully open-source App. How do you feel?

**Q: Why did you contact me via an anonymous E-Mail address?**

A: If we did contact you, it very likely did not happen through a clear name, mail or address. Even a phone call or personal meeting will be highly unlikely. Why? Simply because the whole purpose of this project is to defend peoples right to privacy. And we all know what happens to people who hand out their clear data and stand up to fight for something the state or law enforcement agencies don't want. That does not mean you have to be scared to contribute now. But feel free to take any security measures.

**Q: I noticed that your App uses GPS. Isn't that dangerous?**

A: Let me clarify some of the use of GPS on mobile phones: Ever since the first (feature) mobile phones with GPS technology was introduced, the GPS part/chip of the phone was separated from the processor. With the introduction of more modern (smart) phones, which have their baseband (RF DSP/modem) sepearted from application processor, the GPS part was still separate and communicating with either AP or BP via a serial interface. However, since about 2012, and in particular on Qulacomm Snapdragon based smart phones, they have integrated all three. For example, in the MSM8960 family, the GPS is part of, and directly communicating with/via the modem (BP), and then eventually forwarded to AP. Only that AP/BP are now **both** located on a [PoP](http://en.wikipedia.org/wiki/Package_on_package) chip. And as shown [here](http://forum.xda-developers.com/showpost.php?p=44757676&postcount=6), Qualcomm insists to install all relevant HW for GPS, even if no such functionality is enabled or present in rest of AP FW. Thus Qualcomm modems can never be trusted to not send GPS data to mobile network. It is simply not possible to turn off the GPS on those devices. It's all embedded. In fact in that same post, E:V:A made an experiment, where he found that GPS hartbeat data was still being fed to the debug interface, even if his device (a wifi router) did not have any such features. Welcome to Qualcomm hell! So to summarize, concerns about GPS are not unfounded, but the idea of turning it off is. You simply can't on those chipsets. You can however, rip open your device and physically add/remove the GPS frequency filters.

**Q: Is what you are doing illegal?**

NO. We are not doing anything illegal since we are not destroying anything and are not even manipulating IMSI-Catchers remotely. We are merely constructing an App that reads certain values of your phone and its network, which helps people detect an attack on their privacy. Everyone has the right to know if they're being attacked or not. Have a look at the most trivial thing, the Ciphering Indicator, which displays if your connection is encrypted or not. What, you never saw it on your Android phone? Well, what a surprise: Google never implemented it, although it is required and has been [requested since 2009](https://code.google.com/p/android/issues/detail?id=5353). And this is one of the reasons we are here. Feel free to join us to making this world a better place.