---
title: "Projecting"
date: 2025-03-28
categories:
  - blog
tags:
  - ham radio
  - electronics
  - projects
---

My receiver prototype was not great. But I have been doing other things to lift my spirits.  I'll come back to a receiver design at some point.  But along with getting awards (see [my other post from today]({% post_url 2025-03-28-awards %})), I have been soldering.  Here's a quick rundown:

## My Pride and Joy- the QRP Labs QMX+

I am so happy with this kit.  It was a daunting build, even for someone with as much soldering experience as me.  But the instructions are detailed and can be followed if you are patient and read everything.  Winding wire around toroids to make inductors and transformers is an exercise in patience.  But everything is clearly explained.  As hard of a build as it was, I would recommend this to someone that wanted to build their first "real" transceiver kit.  It is very high performing for the price.  Sure, a $1,000 radio can beat it.  But for about $160 including the case this is one of the best kits to build.  And there is a new firmware out that enables SSB, so given the QMX+'s weight and features, I might take it to the park to try out POTA.

![The QMX+](/assets/images/projecting/qmx.jpg)

## The Chinese projects

You can get a lot of amateur radio stuff from China on sites like eBay or AliExpress.  Most of the electronics stuff isn't that great, but the PRICE IS OUTSTANDING.  So I have built two Chinese kits so far, an ATU-100 automatic antenna tuner with a case I 3-D printed myself to save a few bucks, and a Pixie QRP CW transceiver that only does Morse code and only on one frequency, and only at 3W.  I'll probably actually use the ATU-100 when I need a portable tuner, but the Pixie is just for fun.  Look at how cute it is!  

![The ATU-100 in purple, and the Pixie](/assets/images/projecting/chinese.jpg)

I'm also working on a 70W power amplifier kit from China and it is a mess.  There are resistors that are the wrong value, and the power transitors are definitely used.  I hope I can get it to work after ordering a few of the correct resistors, and if I do you'll see it in action along with the ATU-100 when I need more power while operating portable.

## Homebrew dummies

I first built a 5 Watt dummy load to test the QMX+ so I could transmit power into something without actually radiating- this is my first homebrew project that actually worked.  It is just 20 1/4W resistors in parallel, all 1,000 Ohms each.  That makes a 50 Ohm load that can handle 5W.  And it works fine.  After that, I decided tat I might want a dummy load that can handle more power, so I looked around and foud some 100W rated resistors on Amazon.  They need to be attached to a heat sink or the won't handle 100W for very long, but I found a small heat sink on Amazon and a M3 tap/drill set to bolt things together.  I originally wired it with speaker wire, but the SWR was unacceptable for a dummy load (up to 1.6:1 at 50 MHz), so I used some RG316 coax to wire it and it got a lot better (1.06:1 at 50 MHz).  So now I can transmit at 100W for a few seconds, and 10-20W indefinitely.  If I wanted to transmit at full 100W for longer periods I would definitely need a bigger heat sink.  But this is good enough to test out radios.

![The dummy loads](/assets/images/projecting/dummies.jpg)

## Failures

I have definitely mentioned that my receiver prototype didn't do so well- don't worry, I'm taking the failure in stride.  I also have attempted to make two filters, a 28-29 MHz band-pass filter and a 1.7 MHz high-pass filter, and neither of them worked.  But between these failures I'm starting to get a feel for what kind of things matter in a RF design.  Impedance matters a lot- and perf board has a lot of metallic circles that mess up the impedance of your design.  Capacitance matters- if you're designing a filter with capacitor values of 10-20 pf, and you glue a PCB square down that has a capacitance of 4 pf, you are throwing your design off by a lot.  Parasitics matter- if you are trying to make a low-loss filter, you need to use low ESR (equivalent series resistance) capacitors and good toroids.  These details matter much more in RF design than they do in digital design.  But as I'm failing I'm getting to see how much this matters and avoid them in my next designs.


![The failures](/assets/images/projecting/failures.jpg)

So there you have it- a summary of all the projects that I've done in the last two months.  I'm sure you'll see the QMX+ and the ATU-100 again, possibly a 70W amplifier, and maybe you'll catch a dummy load in use in a picture in the future.