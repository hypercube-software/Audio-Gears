# Yamaha TX-81Z

![image-20250106140424498](assets/image-20250106140424498.png)

# Overview

## Features

The motherboard is build around a FM Tone Generator capable of producing sounds with 4 FM operators and 8 algorithms:

![image-20250106212404938](assets/image-20250106212404938.png)

Each operator can produce one of 8 different waveforms which is a very nice (the DX7 uses only sine waveforms):

![image-20250106211618781](assets/image-20250106211618781.png)

Envelope Generator (EG) is close to an ADDSR: 

- 4 rate parameters

- 1 level parameter

![image-20250106212703281](assets/image-20250106212703281.png)

## Motherboard

![image-20250106210522349](assets/image-20250106210522349.png)

![image-20250106140529934](assets/image-20250106140529934.png)

![image-20250106215508491](assets/image-20250106215508491.png)

- `Yamaha YM2414B`: FM Tone Generator called **OPZ** (see wiki [here](https://en.wikipedia.org/wiki/Yamaha_YM2414))
- `Yamaha YM3012`: 16 bit Stereo DAC
- `Yamaha XB18610`:  64K ROM
- `Toshiba TC5564PL-15`: 8K RAM (see pdf [here](https://www.cryptomuseum.com/spy/fs5000/files/TC5564.pdf))
- `Hitachi HD63B03XP`: Microcontroller 2Mhz (The CPU of the unit)

# Manuals

- Service manual: can be found [here](https://mgregory22.me/tx81z/files/Yamaha_TX81Z_ServiceManual.pdf) and [here](https://schematicsforfree.com/files/Audio/Products/Musician/W-X-Y-Z/Yamaha%20TX81Z%20FM%20Tone%20Generator%20Service%20Manual.pdf).
- Manual in very good quality: [here](https://www.patchmanmusic.com/manuals/TX81z_E-UM_HiQ.pdf)

# Battery replacement

My TX-81Z had a dead battery causing not only to loose the settings but also garbage in the entire R/W memory: patch names and settings are randomly set at each reboot.

The culprit was this little girl:

![image-20250106142258299](assets/image-20250106142258299.png)

Oh boy...

![image-20250106142351099](assets/image-20250106142351099.png)

Here how to replace it with this "button battery holder":

![20250105_183733](assets/20250105_183733.jpg)

You can bought 20 of them on amazon [here](https://www.amazon.fr/dp/B099HX71JX). Note the little switch to enable/disable the battery: don't forget to enable it !

## Unscrew

You first need to remove various screw around the unit:

In the back:

![20250105_175456](assets/20250105_175456.jpg)

On the sides:

![20250105_190822](assets/20250105_190822.jpg)

Jack connectors:

![20250105_175630](assets/20250105_175630.jpg)

You will end-up with something like this:

![20250105_175720](assets/20250105_175720.jpg)

Once the unit is open, you need to remove the screw from the motherboard:

![image-20250106140529934](assets/screws.png)

The Jack connectors have also washers:

![20250105_180037](assets/20250105_180037.jpg)

Pay attention to this screw which is grounded:

![20250105_173551](assets/20250105_173551.jpg)

## Connectors

Then unplug various connectors from the mother board. Use a screwdriver to gently help the connector to extract itself.

Do various rotations on each sides like this:

| ![20250105_174459](assets/20250105_174459.jpg) | ![20250105_174505](assets/20250105_174505.jpg) |
| ---------------------------------------------- | ---------------------------------------------- |



![20250105_173833](assets/20250105_173833.jpg)

![20250105_174143](assets/20250105_174143.jpg)

![20250105_174308](assets/20250105_174308.jpg)

![20250105_174846](assets/20250105_174846.jpg)

![20250105_175027](assets/20250105_175027.jpg)

![20250105_175142](assets/20250105_175142.jpg)

## Open

You can now extract the mother board, from the front of the unit, then from the back. Gently !

![20250105_175838](assets/20250105_175838.jpg)

This is it ! The motherboard is out:

![20250105_175943](assets/20250105_175943.jpg)

Note the black anti-static plate in the bottom.

## Unsolder

You need to unsolder those two points:

![20250105_180522](assets/20250105_180522.jpg)

My desoldering pump damaged a little bit the board, but nothing really serious:

![20250105_182711](assets/20250105_182711.jpg)

Anyway, the first pin of the battery came out easily:

![20250105_182128](assets/20250105_182128.jpg)

Then the other:

![20250105_182612](assets/20250105_182612.jpg)

## Solder

Place the battery holder properly, pay attention to "+" and "-":

![20250105_184811](assets/20250105_184811.jpg)

Then time to solder the two cables:

![20250105_184540](assets/20250105_184540.jpg)

It's not an issue if you touch the big ball.

# Power Switch

My unit still have an issue with the power switch. I plan to fix it later...

- When I push it, the long metallic bar does not a good job to activate the switch
- May be the switch must be replaced or the bar

![20250105_185345](assets/20250105_185345.jpg)

The switch is a regular **SPST** (Single Pole Single Throw): `5A/40A,250V MM-13-1` which is also used in the **DX7**. 

![20250105_185306](assets/20250105_185306.jpg)

By the way, Yamaha call the power transformer **XB359** apparently:

![image-20250106220121320](assets/image-20250106220121320.png)