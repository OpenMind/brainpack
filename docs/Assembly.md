
# PRISM

## Introduction: 

PRISM (Platform for Robotics Integration, Sensing and Modularity) is a complete hardware-software package that provides a generalized and universal hardware configuration to interface with proprietary robotics and expose it to widely used communication routines such as Robotics Operating System (ROS2), CYCLONEDDS, etc. 

Designed with the goal of Human-Robot interaction, PRISM aims to bridge the gap between robotics and software interaction and provide a platform for further development and research.

Included in this document is a detailed set of instructions to fabricate and assemble to a ready-to-develop state. 
Please refer below for hardware specifications, parts requirements and guidelines on 3D printing and custom fabrication.
Additionally, you may refer here for additional information:

[Bill of Materials](./Bill_of_Materials.md)

[CAD Drawings](../cad/)

[Cable Fabrication]

[FAQ](./faq.md)

## Quick Start Guide:

### Prerequisites:
    1. A Unitree Go2 Edu
    
    2. A complete PRISM kit
    
    3. Screwdriver and Allen Key Set [List of Tools]

### Installation Steps:
    1. First, unplug the power and Ethernet cables that plug into the Unitree Go2 proprietary compute unit. 

    2. Remove the compute unit:
        i. Unscrew the 2 screws here (top), and here(back)
        ii. Remove the top lid, and unscrew the 4 screws attaching the lift handle.
        iii. Reattach the lid, and screw in the top and back screws.

    3. Attach the PRISM Base Mount Bracket to the bottom of the PRISM - Backpack. You may use adhesive.

    4. After lining up the screw slots on the PRISM - Backpack:
        i. Use the 25 mm Sockethead Screws to secure the top 2 slots.
        ii. Use the 30 mm Sockethead Screws to secure the bottom 2 slots.
    
    5. Place the AGX Push Fit Bracket into the back of the Backpack Shell, taking care not to disrupt the cabling. 
    
    6. Place the NVIDIA Jetson AGX on top of the bracket, aligning it with the raised pins on the bracket. Push from the top to secure it in place. 
    
    7. Attach the Front Unit to the raised circular mount near the head of the Unitree Go2. You may use adhesive to secure it in place.
    
    8. Connect the peripherals to the Jetson:
        i. Waveshare USB Audio Driver
        ii. RJ45 Ethernet Cable from the Ethernet Hub
        iii. USB C to A Adapter - Intel 435i Depth Camera
        iv. USB B Data Cable - Front Unit USB Hub
        v. HDMI to DP Adapter - HDMI cable for Front Screen
    
    9. Connect the USB C to JST Connector to the Powerboard to power the Front Unit.
    
    10. Connect the Split Power Cable to the Go2 Power Out, and the RJ45 to the Ethernet Board.
    
    11. Plug in the 2.1 mm Power Barrel Jack from the Powerboard into the Jetson AGX.
    
    12. Snap on the the lid, making sure that all cables are secured inside and none are left dangling.
    
    13. Turn on the Unitree Go2.


## Installation Prerequisites

### Parts Overview

| Name | Quantity | URL |
|------|----------|-------|
| Elecrow 5" Display | 1 | [Link](https://www.amazon.com/ELECROW-Raspberry-Touchscreen-Monitor-HDMI-Compatible/dp/B07FDYXPT7) |
| SLAMTec RPLidar | 1 | [Link](https://www.amazon.com/Slamtec-RPLIDAR-Scanning-Avoidance-Navigation/dp/B07TJW5SXF) |
| Logitech Brio 101 | 1 | [Link](https://www.amazon.com/Logitech-Webcam-Meetings-Streaming-Built/dp/B0BXGFFSL1) |
| Coolgear USB Hub | 1 | [Link](https://www.amazon.com/Coolgear-Powered-Port-Surge-Protection/dp/B07G7GP15C/) |
| Gigabit Ethernet Hub | 1 | [Link](https://www.amazon.com/dp/B0D9BN22Z) |
| Waveshare USB Driver | 1 | [Link](https://www.amazon.com/Waveshare-USB-Converter-Raspberry-Driver-Free/dp/B08R38TXXL) |
| UXCell 4 Ohm Speakers | 2 | [Link](https://www.amazon.com/uxcell-Internal-Magnet-Speaker-Loudspeaker/dp/B082ZPP56D) |
| NVIDIA Jetson AGX | 1 | [Link](https://www.amazon.com/NVIDIA-Jetson-Orin-64GB-Developer/dp/B0BYGB3WV4/) |
| 25mm M3 Socket head screws | 2 | [Link](https://www.amazon.com/Kadrick-Aassortment-4mm-40mm-Commonly-Stainless/dp/B0BPFXP2M9/) |
| 30mm M3 Socket head screws | 2 |  [Link](https://www.amazon.com/Kadrick-Aassortment-4mm-40mm-Commonly-Stainless/dp/B0BPFXP2M9/) |
| M3 Washers | 4 |  [Link](https://www.amazon.com/HELIFOUNER-Washers-Stainless-Diameter-Thickness/dp/B0B3RVM92N/) |
| USB C Male PCB Adapter | 2 | [Link](https://www.amazon.com/ANMBEST-Connector-Receptacle-Adapter-Support/dp/B091CRLJM2/) |
| USB A Make PCB Adapter | 2 | [Link](https://www.amazon.com/uxcell-Socket-Connector-Replacement-Adapter/dp/B07R2KNXTS/) |
| Male 4 pin JST Connector cable| 1 | Link |
| | | | 

    
### Tools Overview

The tools provided in the table below are some examples of tested equipment that is recommended for beginners. Experienced users should rely on their own discretion for tool selection. 

**⚠️ Safety Notice:** Please exercise caution when handling tools that involve high temperature or voltage.

| Name | URL |
|------|-----|
| Soldering Iron, Flux and Solder Wire | [Link](https://www.amazon.com/Gorilla-Heavy-Double-Sided-Mounting/dp/B082TQ3KB5/) |
| Glue / Glue Gun | [Link](https://www.amazon.com/Gorilla-8401509-Hot-Glue-Sticks/dp/B07K791YRP/)|
| Wire Strippers | [Link](https://www.amazon.com/haisstronica-Stripper-Automatic-Crimping-Universal/dp/B0B2NWK1QX/)|
| Robust electrical cabling / wires | Link |
| Butt connectors | [Link](https://www.amazon.com/Insulated-Connectors-Sopoby-Uninsulated-Electrical/dp/B0BZ8B3V6Q/)|
| Heat Shrink Tubing | [Link](https://www.amazon.com/Eventronic-Heat-Shrink-Tubing-Kit-3/dp/B0BVVMCY86/) |
| Heat Gun | [Link](https://www.amazon.com/ROMECH-400%C2%B0F-660%C2%B0F-Overload-Protection-Embossing/dp/B0CHVDL25P/) |
| Allen Key Set | [Link](https://www.amazon.com/ELEAD-Hex-Key-Allen-Wrench/dp/B0DJNF75BX/) |
| Screwdriver Set | [Link](https://www.amazon.com/uxcell-Socket-Connector-Replacement-Adapter/dp/B07R2KNXTS/) |
| Strong Double Sided Tape | [Link](https://www.amazon.com/Gorilla-Heavy-Double-Sided-Mounting/dp/B082TQ3KB5/) |
| Pliers | [Link](https://www.amazon.com/WORKPRO-7-piece-Pliers-Diagonal-Linesman/dp/B0105SSMRO/) |
| Multimeter |[Link](https://www.amazon.com/Klein-Tools-MM325-Multimeter-Manual-Ranging/dp/B0B57L9FNL/) |

### Custom Fabrication Guide

This project requires several 3D printed housing parts which can be found in the [CAD directory](../cad/), as well as custom cabling. Provided in this document are reference images for cabling connections as well as basic instructions on how to do so. 

**⚠️ Safety Notice:** Please exercise caution when fabricating wire connections and always remember to do a safety power check before plugging power electronics.

| Part Name | Quantity | Notes |
|-----------|----------|-------|
| USB C to JST Connector | 1 | Power for Ethernet Board |
| 2.1 Barrel Jack Power In Cable | 1 | External Power delivery from Powerboard |
| 2.1 Barrel Jack Power Out Cable | 1 | Powerboard to Jetson AGX |
| Split Power Delivery Cable | 1 | Power from Go2's Battery to 2 Openmind Powerboard PCBs |
| Waveshare Speaker Cable | 1 | Shortened and modified to connect to speakers and fit inside backpack |
| Logitech Brio Webcam USB A Connector | 1 | Shortened the cable from the webcam and connected to USB A |
| 2.1 Barrel Jack to JST Connector | 1 | Power for Coolgear USB Hub |

### 3D Prints

We recommned using a standard **PETG-CF** reel. Carbon Fibre offers minimal interference with wireless connection circuits inside the enclosure.


| Name | Quantity | 3D Model  |
|------|----------|----------------|
| Backpack Shell | 1 | [Link](../cad/Backpack.stl) |
| Backpack Mount Bracket | 1 | [Link](../cad/MountBracket.stl) |
| Jetson AGX Push Fit Bracket | 1 | [Link](../cad/PushFitBracket.stl) |
| Backpack Lid | 1 | [Link](../cad/BackpackLid.stl) |
| Display Bezel | 1 | [Link](../cad/Bezel.stl) |
| Display Bezel Backplate | 1 | [Link](../cad/Backplate.stl) |
| Front Housing | 1 | [Link](../cad/FrontHousing.stl) |

## Main Assembly
    
### Go2 EDU compute attachment removal

**The Unitree Go2 EDU includes an additional compute module mounted on its back. For the purposes of the this guide, we are going to remove it.** 

    1. Unplug the RJ45 cable and power cable coming from the Go2.

    2. Undo the 4 screws holding the module on the top.

    3. Undo the 2 screws holding the module on the bottom.

    4. Gently lift the module and its two mounting bars out of the way.

    5. Undo the 2 screws in the back lift handle connection

    6. Gently remove the top cover of the Go2.

    7. Undo the 2 handle screws at the front lift handle connection.

    8. Remove the lift handle and screw the top cover back on the Go2.

### Backpack

    1. Shorten and prepare the Speakers (by soldering to the JST connector) then snap them into the Speaker groove in the Backpack shell.
        - Uxcell speakers
        - JST connector speaker wire (from waveshare audio driver)

    2. Connect the JST connectors to the Waveshare USB driver.

    3. Remove the Ethernet hub from its enclosure, then slot it into the front slot of the Backpack Shell. You may use Glue to secure it in place.

    4. **(Recommended)** Route the speaker wires so that they are placed behind and under the Ethernet hub to minimize cable congestion.

    5. Prepare the power delivery wires:
        - Split Power cable
        - 2.1 mm Barrel Jack Power In
        - 2.1 mm Barrel Jack Power Out

    6. Place the 2.1 mm Female Barrel in the circular slot, then use the wrench to turn and thread it into the Backpack shell.

    7. Connect all power cabling into the Powerboard (x2) using the screw terminals. Remember to verify polarity.

    8. **(Recommended)** Use a multimeter to verify connections before usage.


### Display Unit

    1. Connect the HDMI and MicroUSB cables to the Elecrow 5" display (connected at the left side).

    2. Snap the display inside the slot in the Bezel. You may use glue to secure it in place.

    3. Place the Logitech webcam in the slot to the right such that the camera and microphone slot into the 2 holes. You may use glue to secure it in place.

    4. Secure the Coolgear USB hub on the side of the Lidar Mount.

    5. Unscrew the legs on the RPLidar, then place the RPLidar on the raised front edge of the Lidar Mount. You may use glue to secure it in place.

    6. Snap in the Display Bezel to the Lidar Mount using the sized slot at the top edge of the bezel. Glue to secure.

    7. Plug in the USB connections to the Coolgear USB hub. There should be 3 USB A connectors connected in the front, with the Type B cable and the Barrel Jack Power In connected at the back.

### Robot Mounting

    1. Attach the PRISM Base Mount Bracket to the bottom of the PRISM - Backpack. You may use adhesive.

    2. After lining up the screw slots on the PRISM - Backpack:
        i. Use the 25 mm Sockethead Screws to secure the top 2 slots.
        ii. Use the 30 mm Sockethead Screws to secure the bottom 2 slots.

    3. Place the AGX Push Fit Bracket into the back of the Backpack Shell, taking care not to disrupt the cabling. 

    4. Place the NVIDIA Jetson AGX on top of the bracket, aligning it with the raised pins on the bracket. Push from the top to secure it in place. 

    5. Attach the Front Unit to the raised circular mount near the head of the Unitree Go2. You may use adhesive to secure it in place.

    6. Connect the peripherals to the Jetson:
        i. Waveshare USB Audio Driver
        ii. RJ45 Ethernet Cable from the Ethernet Hub
        iii. USB C to A Adapter - Intel 435i Depth Camera
        iv. USB B Data Cable - Front Unit USB Hub
        v. HDMI to DP Adapter - HDMI cable for Front Screen

    7. Connect the USB C to JST Connector to the Powerboard to power the Front Unit.

    8. Connect the Split Power Cable to the Go2 Power Out, and the RJ45 to the Ethernet Board.

    9. Plug in the 2.1 mm Power Barrel Jack from the Powerboard into the Jetson AGX.

    10. Snap on the the lid, making sure that all cables are secured inside and none are left dangling.


## Testing and Verification

### Power On

    1. Before turning on the Unitree Go2, make sure that:
        i. The battery is correctly inserted into the robot. Listen for a click.
        ii. There is sufficient charge in the battery.
        iii. All power cables inside the PRISM enclosure are connected correctly and securely. 

    2. Turn on the Go2 by pressing the battery button. Use a short press then a long press.

    3. Once the robot is turned on, it will stand up on its own after a brief startup routine.

    4. Once the startup routine is finished, your Go2 will automatically boot and run OM1. 
    
**Congratulations, you have finished your PRISM setup!**

### Troubleshooting

## Appendix:

### Cable Fabrication Instructions

    1. USB C to JST Connector:
        1. Snap in JST cabling to the Pin Adapter
        2. (Optional) Check polarity on the USB C connector
        3. Using the soldering iron, solder the positive and negative leads of the JST cables to the USB C adapter. Remember to be careful not to apply too much solder and damage the connection.
        4. This USB C adapter will then be connected to the Ethernet Hub's USB C power.
        5. The JST pin adapter will be plugged into the OM1 powerboard. 

    2. 2.1mm Barrel Jack Power Cable (Male)
        1. Measure about 6 cm of cable length from the barrel jack, then cut the rest of the length.
        2. Using the wire strippers, strip out about 2mm of cable from each of the positive and negative ends.
        3. Using the soldering iron, gently tin the cable ends. Be careful not to add too much solder.
        4. Once tinned, screw positive and negative ends onto the screw terminals of the OM1 powerboard.

    3. 2.1mm Barrel Jack Power In Cable (Female)
        1. Measure about 6 cm of cable length from the female power adapter. 
        2. Using the wire strippers, strip out about 4mm of cable from each of the positive and negative ends.
        3. Using the soldering iron, gently tin the cable ends. Be careful not to add too much solder.
        4. Once tinned, screw positive and negative ends onto the screw terminals of the OM1 powerboard.
        5. Place the barrel into the front circular slot facing outwards. Make sure the cable ends are pointed inside the shell.
        6. Using pliers, rotate and thread the barrel into the front circular slot to secure it in place.

    4. Waveshare Speaker Cable
        1. Measure about 11 cm of cable length from the 4 pin JST connector. Each pair will be soldered to one speaker.
        2. Using the wire strippers, strip out about 4mm of cable from each of the positive and negative ends.
        3. Using the soldering iron, solder the positive and negative ends to their respectively marked terminals on the speaker. 
        4. Repeat this so that both speakers are soldered to the JST connector cable.

    5. Logitech Brio Cable
        1. Unbox and ready your Logitech Brio webcam.
        2. Remove the webcam from its housing unit. You should see a thin PCB with the attached camera and mic module.
        3. (Optional) For better cable management, you may shorten the USB cable. In this case, you must solder the power (red and black) and data lines (white and green) to a USB adapter so that it can be connected to the Coolgear USB Hub.

    6. 2.1 Barrel Jack (Male) to USB C Power
        1. Measure about 12 cm of cable length from the 2.1 barrel jack (male) connector.
        2. Using the wire strippers, strip out about 4 mm of cable from each of the positive and negative ends.
        3. (Optional) Verify the correct polarity for the USB C Connector.
        4. Using a soldering iron, solder the positive and negative ends to their respective terminals on the USB C Connector.



### Safety and Testing

- Always verify power connections with a multimeter before first power-on
- Ensure all cables are properly secured and not pinched
- Double-check polarity on all power connections
- Perform initial power-on test with monitoring equipment ready


## Support

If you encounter any issues during assembly, please:
1. Check the [FAQ section](./FAQ.md)
2. Open an issue in this repository
3. Contact our support team

---

   
