This is our non-geeky page explaining everything in easy words. Enjoy!

![Header](https://github.com/SecUpwN/Android-IMSI-Catcher-Detector/blob/master/DOCUMENTATION/GeneralOverview_Header.jpg)

In principle we need to identify the differences between standard operations of legit cell networks and the behavior of fake Base Stations (IMSI-Catcher). 

The basic strategies of the detection mechanisms are:

* Check the identity of the Base Station (the device your cell phone is connected to).
This is basically the main failure when the GSM standard was developed, more than 20 years ago. Because there is no function or component that ensures a connection with a real Base Station. 
So what our App does is check the parameters of the Base Station received by the cell phone against databases from the Internet. These databases where collected by open source projects (like [OpenCellID](http://opencellid.org/)) and can be used free of charge. 
The first validation we have implemented checks if the ID and the geographic location belong to the network of your provider. More verifications will be realized in the near future.

* Find unusual behaviour of the Base Station. This can be achieved with analysing statistic calculations. 
A suddenly rising signal strength to an unusual level can be caused by an IMSI-Catcher. Therefore we need measurements under certain conditions over a longer period of time. 

* Another way to find unusual behaviour can be obtained by analysing the protocol of the current connection. But this is not supported by the network or by the cell phone.  So this is the heavy part in our development and we are working hard on those issues. While every smartphone brand has a slightly different way of internal working, there is a lot of research to do in this field. Therefore, please help us and submit your findings!
