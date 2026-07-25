# TQ-5

![image-20260725190316749](assets/image-20260725190316749.png)

# Overview

The Yamaha TQ-5 is the desktop version of the YS-200. 

**Synthesis Engine:** 4-Operator FM Synthesis (OPZ / YM2414 chip family, similar to the TX81Z and DX11)

**Polyphony:** 8 voices

**Multitimbral / Parts:** 8 parts

**Algorithms:** 8 algorithms

**Waveforms:** 8 standard waveforms (Sine, All positive sine, Direct sine, etc.) plus user-selectable operator waves

**Sequencer:** 8-track sequencer with real-time and step recording, and built-in pattern/song memory

**Effects:** Built-in digital effects processor (Reverb, Delay, Distortion, Echo)

**Presets:** 100 preset voices, 100 internal user voices, 100 multi-setup memories (Performances)

**Storage / Expansion:** Yamaha MCD32 or MCD64 Memory Card slot, MIDI Data Dump support

**Display:** Backlit LCD screen

**Controllers / Interface:** Unique front-panel layout with directional buttons and a data entry slider designed for desktop operation

**Connections:**

- MIDI In, Out, Thru
- Stereo Audio Output (L/Mono, R)
- Headphone jack
- Sustain pedal input

# PCB

**This unit is a real pain to open** due to 4 "grounded" screws on top right and top left. Be patient. don't rush.

![image-20260725213317762](assets/image-20260725213317762.png)

![image-20260725195453412](assets/image-20260725195453412.png)

## ROM

![image-20260725191018851](assets/image-20260725191018851.png)

The firmware is located in **IC6** which is a Toshiba EPROM: TC571000D-20. This chip contains the sounds.

## SRAM

The user presets are stored in **IC7** and contains 8KBytes of memory.

![image-20260725191342841](assets/image-20260725191342841.png)

## Glue Logic

The **XF148A0** is a custom ASIC/Gate array. It acts as a hardware bridge that handles data routing and communication between the main microprocessor, the front-panel interface (buttons and display), and the internal system buses, significantly reducing the need for discrete logic components on the motherboard.

![image-20260725191824622](assets/image-20260725191824622.png)

## FM  chip

![image-20260725192224046](assets/image-20260725192224046.png)

**IC12** is the legendary **4-operator FM synthesis sound chip YM2414B** (known as the **OPZ**), which is the core sound engine of the TQ-5 and many other Yamaha synths.

![image-20260725224025031](assets/image-20260725224025031.png)

The digital signal (floating point samples) is serialized through 2 bits: **SH1** and **SH2**

## LDSP

This chip is responsible for **Delay** and **Reverb**.

![image-20260725222536363](assets/image-20260725222536363.png)

**IC13** is the **YM3413** which receive the digital waveforms from the **YM2414B** and send back the signal to the final DAC.

**NOTE**: the audio signal is **serialized** through 2 bits. This chip receive it in **SI0** and **SI1** and output it through **SO0** and **SO1**.

![image-20260725222837821](assets/image-20260725222837821.png)

It can be found in the SY77, TG100 or PSR-510

## Weird DAC

![image-20260725192823957](assets/image-20260725192823957.png)

**IC15** is the Digital to Analog converter of the TQ5 often called DAL: **Yamaha YM3017**. It can be found also in the Yamaha YS200 or V50 service manual.

![image-20260725222018116](assets/image-20260725222018116.png)

![image-20260725221147692](assets/image-20260725221147692.png)

Some info can be found in **Yamaha HS Series Organ IC Data book**, I was not able to found the official datasheet of this model (YM3015 and YM3020 can be found).

![image-20260725194028315](assets/image-20260725194028315.png)

Apparently it acts as the **YM3015** or **YM3020**, it is a 2 bit serial input receiving **4 floating point numbers**.

![image-20260725194220316](assets/image-20260725194220316.png)

Therefore, the chip provides **4 analog outputs** whereas **YM3015** and **YM3020** provide only 2 analog outputs.

This is very weird because the TQ-5 and YS-200 use only 1 stereo output.

# Battery replacement

## Dismount

After removing the screw on left and right...

![image-20260725213603301](assets/image-20260725213603301.png)

I had only ONE ribbon to unplug, and the whole PCB open like a book:

![image-20260725213754803](assets/image-20260725213754803.png)

The red circle indicate where the battery need to be unsoldered

## The original

Same story than **TX-81Z**: the battery need to be unsoldered to be changed. It is a **CR2450**:

![image-20260725195538607](assets/image-20260725195538607.png)

You have to remove the first PCB to be able to properly unsolder the battery holder from the back:

![image-20260725195858544](assets/image-20260725195858544.png)

Be ready to struggle !

![image-20260725213004164](assets/image-20260725213004164.png)

![image-20260725195628332](assets/image-20260725195628332.png)

## Replacement

You can buy a bunch of CR2450 holders made by "sourcing map" on amazon [here](https://www.amazon.fr/dp/B07JLY8S4N).

![image-20260725211503616](assets/image-20260725211503616.png)

Aligning the pin on the hole is not very difficult

![image-20260725211823962](assets/image-20260725211823962.png)

Make sure you don't touch the components around, you should have just enough space.

![image-20260725212049120](assets/image-20260725212049120.png)

You will solder from the back of the PCB. It is not very easy to do because we have only two hands ! 

![image-20260725212549567](assets/image-20260725212549567.png)

**NOTE**: we use only two holes in the PCB, the third one is left "as is"

The battery holder should be now very close to the PCB.

![image-20260725212220849](assets/image-20260725212220849.png)

## Final result

![](assets/image-20260725211312615.png)

Note how the diode on the right is very close, so don't try to squeeze the battery holder on the PCB, you may damage it !
