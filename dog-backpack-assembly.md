# PRISM Assembly Instructions

## Hardware Requirements

Please refer to this document for hardware specifications, parts requirements and guidelines on custom fabrication.

Additionally, you may refer to these links for additional required information:

- [Bill of Materials](./BOM.xlsx)
- [CAD Drawings](../cad/)

## Parts and Components

### Electronics

There are several off-the-shelf components and electronics that may be used. We strongly recommend using only the parts listed in the Bill of Materials.

#### List of Electronics and 3rd Party Hardware

| Name | Quantity | Notes | URL | Image |
|------|----------|-------|-----|-------|
| Elecrow 5" Display | 1 | | | |
| SLAMTec RPLidar | 1 | | | |
| Logitech Brio 101 | 1 | | | |
| Coolgear USB Hub | 1 | | | |
| Gigabit Ethernet Hub | 1 | | | |
| Waveshare USB Driver | 1 | | | |
| UXCell 4 Ohm Speakers | 2 | | | |
| NVIDIA Jetson AGX | 1 | | | |

### Custom Fabrication

This project requires several 3D printed housing parts which can be found in the [CAD directory](../cad/), as well as custom cabling. Provided in this document are reference images for cabling connections as well as basic instructions on how to do so. 

**⚠️ Safety Notice:** Please exercise caution when fabricating wire connections and always remember to do a safety power check before plugging power electronics.

#### Required Tools

| Name | URL | Image |
|------|-----|-------|
| Soldering Iron, Flux and Solder Wire | | |
| Glue / Glue Gun | | |
| Wire Strippers | | |
| Robust electrical cabling / wires | | |
| Butt connectors | | |
| Heat Shrink Tubing | | |
| Heat Gun | | |
| Allen Key Set | | |
| Phillips Head Screwdriver | | |
| Strong Double Sided Tape | | |
| Wrench | | |
| Multimeter | | |

#### 3D Printed Parts Required

| Name | Quantity | CAD Model Link | Image |
|------|----------|----------------|-------|
| Backpack Shell | 1 | | |
| Backpack Mount Bracket | 1 | | |
| Jetson AGX Push Fit Bracket | 1 | | |
| Backpack Lid | 1 | | |
| Display Bezel | 1 | | |
| Lidar Mount | 1 | | |

#### Custom Fabricated Cabling Required

| Part Name | Quantity | Notes | Image |
|-----------|----------|-------|-------|
| USB C to JST Connector | 1 | Power for Ethernet Board | |
| 2.1 Barrel Jack Power In Cable | 1 | External Power delivery from Powerboard | |
| 2.1 Barrel Jack Power Out Cable | 1 | Powerboard to Jetson AGX | |
| Split Power Delivery Cable | 1 | Power from Go2's Battery to 2 Openmind Powerboard PCBs | |
| Waveshare Speaker Cable | 1 | Shortened and modified to connect to speakers and fit inside backpack | |
| 25mm M3 Socket head screws | 2 | For mounting the backpack on the front of the Go2 | |
| 30mm M3 Socket head screws | 2 | For mounting the backpack on the back of the Go2 | |
| Logitech Brio Webcam USB A Connector | 1 | Shortened the cable from the webcam and connected to USB A | |
| 2.1 Barrel Jack to JST Connector | 1 | Power for Coolgear USB Hub | |

## Assembly Instructions

### Part 1: Display Unit Assembly

1. Connect the HDMI and MicroUSB cables to the Elecrow 5" display (connected at the left side).

2. Snap the display inside the slot in the Bezel. You may use glue to secure it in place.

3. Place the Logitech webcam in the slot to the right such that the camera and microphone slot into the 2 holes. You may use glue to secure it in place.

4. Secure the Coolgear USB hub on the side of the Lidar Mount.

5. Unscrew the legs on the RPLidar, then place the RPLidar on the raised front edge of the Lidar Mount. You may use glue to secure it in place.

6. Snap in the Display Bezel to the Lidar Mount using the sized slot at the top edge of the bezel. Glue to secure.

7. Plug in the USB connections to the Coolgear USB hub. There should be 3 USB A connectors connected in the front, with the Type B cable and the Barrel Jack Power In connected at the back.

### Part 2: Backpack Electronics Assembly

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

### Part 3: Final Assembly

1. Remove the Standard compute unit that comes included with the Unitree Go2 Edu

2. Connect the Back Mount Bracket to the base of the Backpack Shell so that the two snap together.

3. Place the Mount Bracket on the back of the Unitree Go2 Edu, aligning the 4 screw slots on the shell with those on the Unitree Go2 Edu.

4. Use 25 mm M3 Sockethead screws to screw in the **front** 2 screws.

5. Use 30 mm M3 Sockethead screws to screw in the **back** 2 screws.

6. Place the AGX Push Fit Bracket into the back of the backpack shell, taking care not to damage the electronics or cabling.

7. Place the NVIDIA Jetson AGX on top of the 4 pins on the AGX Push Fit Bracket. Push from the top to secure it in place.

8. Connect the Split Power Cable to the Go2 Power Out, and the RJ45 Cable to the Ethernet board.

9. Connect the peripherals to the Jetson:
   - Waveshare audio driver
   - USB C to A Adapter and the Intel d435i
   - USB C Data cable from the Display Unit
   - HDMI to DP Adapter and the HDMI Cable from the Display unit

10. Plug in the 2.1 mm Power Barrel Jack to the Jetson Power In.

11. Snap on the lid, making sure that all cables are secured inside the backpack and none are left dangling outside.

12. Turn on the Unitree Go2.

## Safety and Testing

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

*Document Version: 1.0*  
