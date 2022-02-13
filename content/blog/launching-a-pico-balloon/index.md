---
title: Launching a Pico Balloon!
featured_image: /images/featured/IMG_4274.JPG
date: 2019-07-13
---

Over the last few months I've been working on building a pico balloon payload for the university society I've been president of, [TinkerSoc](http://tinkersoc.org). 

This has been my first foray into designing PCBs and writing code for (just) the ATMega328PU, so it's taken a little while! 
For communications, I decided LoRa (the 433MHz version, and not to be confused with LoRaWAN - this is raw LoRa) would be the best choice - it's in the licence free ISM band, modules are relatively cheap and it has great range. 
For processing the ATMega328PU was chosen simply because I have experience with the Arduino ecosystem. 
For temperature, the LM75B was chosen - again because I have experience with it. 
And the serial Ublox NEO6M GPS modules, which are very easy to find cheaply on Aliexpress were chosen simply because of their price. 

I did a little testing with LoRa modules between two Arduinos before starting out to check they'd be right for the project. I also found the [loratracker](http://www.loratracker.uk/) project - and was intially going to just build one of their boards, but thought it would be more fun to build my own. 

Here's the schematic for my board: {{% picture "launching-a-pico-balloon/Screenshot%202019-07-13%20at%2010.49.13.png" %}}

And here's the routed PCB (fills hidden): {{% picture "launching-a-pico-balloon/Screenshot%202019-07-13%20at%2010.57.00.png" %}}

I used [JLCPCB](http://jlcpcb.com) for the PCB fabrication - again because of cost - the boards that they produced seem good to me! Here's the fabritcated PCB: {{% picture "launching-a-pico-balloon/IMG_4010.JPG" %}} 

And here's it assembled! {{% picture "launching-a-pico-balloon/IMG_4274.JPG" %}}

Unfortunately, after many days of testing, it was determined that this payload would not be launchable by the time that we wanted - end of term. This is because the data the GPS was sending was not being processed properly by the hardware/software. The probable cause of this is the use of the internal oscialltor on the ATMega, causing problems with the serial timing. 

## Actually launching! 

Instead of using this board for the launch, we used an ESP8266, the same GPS module and a spare LoRa module (not an RFM96W - but it worked fine). 
We immediately found, within a day of work, that all these components worked well together when powered via a power supply! 
{{% picture "launching-a-pico-balloon/IMG_4383.JPG" %}}
During testing it was found that only using a single battery was problematic, as we were drawing too much current. 
Adding a second in series helped thankfully. Next time batteries designed for higher current draw would need to be chosen. But we got it working - so we launched! 

Here's the map of where the payload went: [https://willfurnell.com/cool_stuff/map.html](https://willfurnell.com/cool_stuff/map.html) 

{{% picture "launching-a-pico-balloon/IMG_4378.JPG" %}}
{{% picture "launching-a-pico-balloon/IMG_4384.JPG" %}}
{{% picture "launching-a-pico-balloon/64684503_610352619374438_23370201252757504_n%281%29.jpg" %}}
{{% picture "launching-a-pico-balloon/64392853_325770328345119_5499845466663157760_n.jpg" %}}
{{% picture "launching-a-pico-balloon/64362887_447445099386604_1985800476020441088_n.jpg" %}}