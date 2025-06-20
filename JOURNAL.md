---
title: "FLIP (Folding Linux-based Interactive Platform)"
author: "Guy Sandler (@guy)"
description: "DS style console made from a compute module"
created_at: "2025-06-12"
---

## Idea:

the pi can run a lot of games + streaming, what if I turn it into a portable console.

I was torn between handheld or DS style, but went with DS because it's compact and I have 2 places to put stuff.

potencial detachable controllers idea.

potencial trackpad and speakers

## part reasearch (june 12 1pm-9pm, worked for about 6.5 hours):

### computer
I have pis but they are way too thick with too many IO I don't need

Compute modules exist and look good

https://www.amazon.com/dp/B0CJ2K6F7Q orange pi compute module 4 8gb 64gb storage, 60$, good but pi4 level

https://www.amazon.com/dp/B0DPJWX59Q orange pi compute module 5 4gb 32gb storage, 87$, low storage and ram, expensive

### buttons
I aimed for free shipping

https://www.aliexpress.us/item/3256804784951471.html 6x6mm buttons, 2.37/2.57$, 20 count

https://www.aliexpress.us/item/3256808376799054.html 12x12x4.3mm buttons, 2.02/2.22$, 20 count

may need some extra reasearch and I might use some I have

### screens
depending on budget I can go for diffrent quality

https://www.aliexpress.us/item/3256805985868271.html 5 inch IPS, 25.17/33.83$, 800x480, serial

https://www.aliexpress.us/item/3256808738957825.html 3.5 inch LCD, 17.64/28.04$ 450x320, with fan, serial in

https://www.aliexpress.us/item/3256806171406643.html 4 inch LCD, 20.62/24.49$, 320x480, serial, has touchscreen option

https://www.aliexpress.us/item/3256806072260865.html 3.2 inch IPS, 10.16/10.36$, 240*320, serial

### joystick
https://www.aliexpress.us/item/3256805297984155.html .97$ 5 pin

I really need to find better ones, all I can find are ribbons and replacements for consoles

I need to somehow find vertical buttons for sholder stuff

## part reasearch 2 (june 13):

9AM:

computer picked: https://www.amazon.com/dp/B0CJ2K6F7Q orange pi compute module 4 8gb 64gb storage, 60$ or 69$ with dev board

4 inch serial screen 480x320 https://www.amazon.com/DWEII-480x320-Display-ST7796S-Compatible/dp/B0CQXDXVPS 18$, looks to be the same but cheaper

every joysick I find has side pins and can't go on a pcb :(

2PM:

I found some 100 pin connectors, they are all from suspicous places

https://www.aliexpress.us/item/3256804813526424.html 7.98/8.40$ + 4.65

https://www.aliexpress.us/item/3256804515010680.html 12.82/21.36$ + 3.97

https://www.aliexpress.us/item/3256808529916053.html 9.66/11.37$ + 4.77

https://www.aliexpress.us/item/3256806302739780.html 1.63$ + 4.11

I made some mochups of console to see what parts I need

![top](/journalimgs/top.png "top")
![bottom](/journalimgs/bottom.png "bottom")

2:55 PM: I am in a dillema, do I use an existing board which adds thichness or go through the pain of making a mount for the CM4 becuase I need GPIOs

4PM: considering a normal orange pi 4 becuase it's somehow cheaper and wayyy easier to intigrate

4:25 PM: WHY IS THERE NO 8GB RAM VERSION

4:42 considering going back to rasperry pi due to software compatibility

5PM: my next best move is a used pi4 8gb 70$ https://www.ebay.com/itm/146206088222 or pi 5 4gb 5https://www.ebay.com/itm/186268654816

started working on battery, I need a battery, charger, and meter

1.86/3.72$ charging board https://www.aliexpress.us/item/3256807619448309.html

batteries are so confusing to make

## part reasearch 3 (june 14, scattered hours, 2-3 hours):

Batteries:

https://www.aliexpress.us/item/3256807240337338.html 13.03/45.17$ 2S 7.4V 3600mah

https://www.aliexpress.us/item/3256807801023707.html range

https://www.aliexpress.us/item/2255800287456634.html range, cheaper

https://www.aliexpress.us/item/2255800287456634.html 7200 but sketchy

USBC modules for charging:

~~https://www.aliexpress.us/item/3256805170308324.html 1.40/4.98$, might not have balancing~~

~~https://www.aliexpress.us/item/3256806796332131.html 1.16/2.33$, looks same as above~~

~~https://www.aliexpress.us/item/3256806810933610.html 2.05/2.25$, might not have balancing, smaller~~

those don't have balancing

I might need to look at a few BMS:

https://www.aliexpress.us/item/3256807828297140.html 2s 20a 1.07/3.57$

## part reasearch 4 (june 15):

I need to cboose a battery

10:06 AM: charger: https://www.aliexpress.us/item/3256806853388654.html 1.41/2.82$ 2s balanced but small

came back 2:02PM

2:24: https://www.aliexpress.us/item/3256806060466442.html BMS 1.22/4.29$ no balance but probablt balance, there are cheaper ones but the others are more skechy

2:57: after digging through a lot of step down modules that don't have the amps I found a good one but it's ac->dc

2:23: finally found something https://www.aliexpress.us/item/3256805862985136.html 5A, I think this one is actually perfect

2:44: for some reason all the on off buttons are huge

2:51: ~~https://www.aliexpress.us/item/3256803806710565.html cool switch 1.74/1.94$~~ it's a push

3:05: https://www.aliexpress.us/item/3256808591861621.html

actually screw it this is too skechy I'll just use a normal power bank, it costs the same anyway and can't turn into a fire bomb

## part reasearch 5 (june 16):

trustworthy 10000mah from adafruit but 40$

had to spend a lot of time looking for a good cheap powerbank

BOM so far:
- https://www.aliexpress.us/item/3256808376799054.html 12x12x4.3mm buttons, 2.02/2.22$
- https://www.aliexpress.us/item/3256807375670744.html 2 5pin joystick 1.56/1.76$
- 2x https://www.waveshare.com/pi5-display-cable.htm?sku=25943 DSI display cables 15pin to 22pin 1.89
- 2x https://www.waveshare.com/product/displays/lcd-oled/lcd-oled-2/43h-800480-ips.htm?sku=24159 4.3 DSI display, 25/30$ no touch/touch
- https://www.amazon.com/INIU-Portable-20000mAh-High-speed-Flashlight/dp/B07YPY31FL 20k 30/27$ OR https://www.amazon.com/INIU-Portable-Charging-10000mAh-Tablets/dp/B09176JCKZ 10k 21$
- https://www.aliexpress.us/item/2255801012106911.html 1.55/1.84$ 10x 1x20 female pin sockets

7:19pm started pcb schematic

7:33pm finished

![schematic](/journalimgs/schematic.png "schematic")
