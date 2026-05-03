<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->
- [BrainPack Build Guide](#brainpack-build-guide)
   * [1. Introduction](#1-introduction)
   * [2. Prerequisites](#2-prerequisites)
   * [3. Assembly](#3-assembly)
      + [3.1. Face Unit](#31-face-unit)
      + [3.2. Face Back](#32-face-back)
      + [3.3. Arducam Camera](#33-arducam-camera)
      + [3.4. Internal Cabling](#34-internal-cabling)
      + [3.5. Thor Cradle](#35-thor-cradle)
      + [3.6. Attaching the Head](#36-attaching-the-head)
<!-- TOC end -->

<!-- TOC --><a name="brainpack-build-guide"></a>
# BrainPack Build Guide

<!-- TOC --><a name="1-introduction"></a>
## 1. Introduction

The BrainPack is a module that can be attached to various robots (such as the Unitree G1 and Go2, as well as the LimX Tron 1). As long as your robot provides power and can interface with external computers, most typically via an Ethernet cable, then the BrainPack should work for your robot. The BrainPack expects developer access to the robot and therefore will not work with toy/entertainment versions of the above robots (such as the Unitree Go2 Air).  

The BrainPack is designed for Human-Robot interaction research and pilot testing. The BrainPack allows you to rapidly test new combinations of advanced compute, new types of sensors, and new types of outputs and actuators. 

**NOTE: The correct assembly of, and safe use of, this research tool requires a fully equipped electronics test and assembly space with all the needed tools and equipment, such as soldering irons, hot glue guns, PCB reflow, crimp tools, multimeters, lab power supplies, thermal imaging (to monitor thermals), and other generic electronics and robotics test and assembly infrastructure.**

**NOTE: this write up is a high-level summary of the central steps required to assemble and use the BrainPack. We assume advanced familiarity with robotics hardware, associated actuators, batteries, and sensors, 3D printing, and related capabilities. The overall assembly process involves more than 300 specific steps. We only provide the most important ones in this write up. Robotics engineers will be able to follow along with minimal difficulty. If you have any questions please reach out to our engineers.**

[Materials](../docs/Materials.md)

[CAD Drawings](../CAD/)

<!-- TOC --><a name="2-prerequisites"></a>
## 2. Prerequisites

1. A Unitree Go2 Edu (for example)

2. All the needed [Materials](../docs/Materials.md)

3. An electronics and robotics rapid prototyping and development lab

<!-- TOC --><a name="3-assembly"></a>
## 3. Assembly

Regardless of movement platform (Unitree G1, Unitree Go2, LimX Tron 1) the system consists of (1) an Nvidia Thor mounted to the robot via a 3D printed cradle, and (2) a face unit. The "face" combines a screen, microphone, speakers, and other electronics. Users may add additional sensors such as a wide field RGB camera (e.g. an Arducam) or a sunlight resistant laser scan unit. 

The face is the most difficult part to assemble. Once assembled, the face is either connected directly to the robot (such as for the Unitree G1) or it is connected to the "head", which also houses cables and provides support for additional sensors. 

<!-- TOC --><a name="31-face-unit"></a>
### 3.1. Face Unit

The face unit is composed of two 3D printed parts (the face bezel and the face back) and a variety of printed circuit boards, sensors, speakers, and other electronics. The face unit is easy to open and close through M3 cap screws.

1. Start with the 3D printed face bezel. 

2. Take the LCD screen and plug a 90° USB cable into the "touch" USB-C connector. 

3. Attach the 90° angled HDMI cable to the LCD screen. Route the cable up and bend it sharply so it lies flat on the LCD PCB. 

4. Peel off the screen protection film. Use hot glue to secure the LCD display in the face bezel.

5. Connect the two cables coming from the LCD display (touch and HDMI) to a computer, so that the screen turns on. Use the LCD screen configuration buttons (on the right side of the screen) to navigate to the brightness menu and adjust the brightness to 100%. These buttons will soon be inaccessible. We generally leave the screen at maximum brightness. Unplug the LCD screen and place it into the face bezel. Use hot glue to secure the LCD screen to the face bezel.

6. Use hot glue to secure the two speakers into the face bezel. Make sure to choose a good angle for the plus and minus speaker hook up lugs. In general, the speaker hook up lugs should point towards the middle of the face bezel for subsequent good soldering access for the speaker hook up wires.

7. Use hot glue to secure the RealSense 435i camera into the face bezel. Connect the 3.1 USB-C to USB-A cable to the RealSense. Use a dab of hot glue to provide strain relief to the USB cable.

8. Use permanent double sided Gorilla mounting tape to secure the 12S buck converter to the right inside cavity of the face bezel. Short the 12V bridge pins on the 12S buck converter to set it to 12V output rather than the default 5.2V. Use mil spec Teflon coated hook up wire (40cm length) to create a power cable for the 12S buck converter input power, and solder the ends to the 12V input of the buck converter. 

9. Use large electronic snips to cut off the bulky RCA stereo output connectors from the audio amplifier PCB. Otherwise, the RCA connectors will conflict with the rest of the assembly. Make sure to remove any dangling or superfluous pieces of metal; you want a clean PCB.

10. Turn over the audio amplifier, remove the volume knob, nut, and washer, snap the PCB in place with the volume adjuster projecting through the side of the bezel, and then mechanically secure the PCB to the bezel with the volume knob nut and a washer. At this point you should be looking at the back of the PCB of the audio amplifier. Now, directly solder connections (1) from the 12V power IN of the audio amplifier to the 12V OUT of the buck converter, and (2) from the signal out of the audio amplifier (left GND and +, and right GND and +) to the two speakers. **CAUTION: ensure that wires are routed in the flattest possible manner and make sure that the wires are not shorted by protruding pins**. Use hot glue and fabric electrical tape to secure the wires; press the fabric electrical tape into the still soft hot glue to generate securely mounted wires that will resist vibrations and strain.

11. Connect the right-angled side of the stereo audio cable to the 3.5mm jack of the audio amplifier.

12. At this point, the face bezel will have five cables coming from it:

* the two power lines (red and black) going to the buck converter
* the 3.5 mm jack stereo input cable 
* the USB-A touch/power cable to the LCD screen 
* the HDMI cable
* the USB 3.1 cable going to the RealSense camera

<!-- TOC --><a name="32-face-back"></a>
### 3.2. Face Back

1. Take the 3D printed face back. 

2. Attach the SMALLRIG Cold Shoe Mount Adapter with the provided three screws. Two of these are very small and one of these is a larger 1/4 bolt. These screws will be hard to get started into the 3D printed material unless you use a hobby knife to slightly open/roughen the hole openings. 

2. Insert 5 ea. M3 threaded brass inserts into the face back with a soldering iron or a heated insert positioning tool.

3. Connect the Comica directional microphone to the face back via the SMALLRIG cold shoe. Connect the 3.5mm TRS cable to the directional microphone. The right-angled end of the TRS cable goes into the back of the microphone. The straight connector will subsequently be plugged into the DAC.

4. Use 4 ea. M3x20mm cap screws to secure the face back to the 3D printed head. Use washers and nylon lock nuts to ensure that the face back does not separate from the head. 

5. Thread all five cables from the face through the face back aperture into the head. Use 5 ea. M3x8mm cap screws to secure the face to the face back.

6. Thread the 3.5mm TRS cable (straight side) through the small microphone cable opening on the side of the head.

<!-- TOC --><a name="33-arducam-camera"></a>
### 3.3. Arducam Camera

1. Connect the Arducam to a computer and confirm correct focus of lens. Manually adjust the focus of lens as needed to achieve a sharp image.

2. Use hot glue to secure the Arducam PCB into the 3D printed enclosure. Manually build a replacement USB cable to connect the Arducam to a USB-A hub. The cable that comes with the camera is typically far too long. Use hot glue to firmly connect the camera cable to the camera enclosure to provide strain relief.

3. Use permanent Gorilla double sided sticky tape to mount the Arducam to the top left of the face unit. If you would like to change the angle of the Arducam, 3D print a small wedge and insert that between the camera and the face unit. 

4. Finally thread the Arducam USB cable through the large hole on the side of the head.

<!-- TOC --><a name="34-internal-cabling"></a>
### 3.4. Internal Cabling

1. At this point you have many wires going into the head. Generally, those will terminate in USB-A connectors or consist of simple hook up wire. Connect all USB connectors to appropriate powered USB hubs to optimize power delivery and data transmission rates. It appears difficult at first, but there is just enough space to correctly route all cables in the head. Once you have achieved good cable routing, close the head with the provided head lid, which also serves as the mount for the RPLIDAR S2. If you feel you do not have sufficient space inside the head manually fabricate more compact USB and power cables.

2. For powering the USB hubs use the barrel jacks and connect them to 12V power converters according to your personal preference.

3. For powering the 12S power converter inside the face, connect the two power cables to your custom power cabling according to your own preference. We generally recommend not to solder any connections, but to use butt crimp connections and mil spec heat shrink tubing with internal adhesive. Minimize the length of any cabling and maximize the AWG of the cable to achieve a mechanically robust and safe power harness.

4. This power harness should also provide power to the Nvidia Thor. Consult the Nvidia developer documentation to determine which wires of the four pin Thor power connector to connect to your custom power harness.

<!-- TOC --><a name="35-thor-cradle"></a>
### 3.5. Thor Cradle

1. Remove the secondary compute module from the back of the Go2 EDU (if present). Remove the Unitree black and white power cable, which we recommend replacing in its entirety with a custom power cable with the correct length. However, retain the short Ethernet cable.

2. Use the two M3x35mm cap screws with washers to secure the FRONT of the 3D printed Thor cradle to the back of the Go2. Use the two M3x50mm cap screws with washers to secure the REAR of the Thor cradle to the back of the Go2.

3. Thread a nylon holding strap through the two provided apertures of the Thor cradle.

4. Snap the two side plates into the Thor cradle. Note these side plates are not identical, but there is a left side plate and right side plate. Inspect the curvature of the Go2's back and then snap in the side plate that fits conformally. These side plates can be used to more securely hold the Nvidia Thor. We sometimes leave them off when we need extra space between the head and the Thor to adjust or check cables, for example.  
5. We recommend removing the Unitree LiDAR underneath the dog's chin. This standard LiDAR is heavy, loud, and has a low frame rate. You can fill the resulting hole under the chin of the dog with a 3D printed adapter, for example a hook or a simple gripper that allows the dog to carry small objects, bones, and bags, helping to solve the last mile delivery problem (for example).

<!-- TOC --><a name="36-attaching-the-head"></a>
### 3.6. Attaching the Head

1. Use hot glue to attach the head to the front top of the dog. Do not drill into the Go2's head since this is where the Go2's internal WiFi antenna is located.

## 4. Other Robots

### 4.1. LimX Tron 1

The assembly of the BrainPack for the LimX Tron 1 is almost identical to the process for the Unitree Go2. The main exceptions consist of the power delivery system since the LimX provides 24V only. Change your power harness as needed/desired. Also, with the LimX Tron 1 the Thor compute unit is placed directly on top of the Tron 1 and a custom 3D printed adapter with M5 T-Slot nuts and bolts is used to support the head. 

### 4.1. Unitree G1

For the Unitree G1 a special face back is used to directly mount the face to the front of the G1. Remove the Velcro-secured G1 plastic chest plate and drill two holes through the plastic chest plate. Then secure the face to the chest plate with 2 M6 bolts with nylon lock nuts. You will need to remove small amounts of foam with a hobby knife from the G1's front plate backing foam to provide space for the nylon lock bolts. 

**Congratulations, you have finished your BrainPack assembly and installation!**