# Bill of Materials and Assembly Notes
[//]:# (**v 0.2**)

# HAZARD/DANGER/CRITICAL: Power Budget

**In general, you should be aware that regardless of robot, you might be operating the system clearly above its design power budget. Solution: careful design consideration of the robot's intend use, average and peak power requirements, and sensor//model/robot interplay** 

Unless you get this right, you will notice fast battery drain, intermittent faults and resets, electrical shorts and fires, overheating, poor sensor performance and many other possible problems. For example a problem could be that if your robot tries to speak and walk at the same time, while running multiple large policies, this could overload the power system, resulting in a power glitch and the robot crashing to the floor. Debugging individual subsystems will not reveal this problem, which only occurs when the robot wishes to move, think, and speak at the same time. 

Solution: Depending on which software you are running, which functionality you wish to support, and how your sensors and Thor are configured, you need to carefully analyze your solution's **ACTUAL** power budget. First, **measure** the actual power draw for your sensors in your specific configuration, and then design and build a suyitalbe power augmentation system and needed power converters. For example, for the Unitree G1 we add an extra battery to the robot, or we add buck regulators as needed. 

**CAUTION/NOTE: adding extra mass to the robot will affect your motion policies and the robot's stability and ability to navigate terrain. Solution: train custom motion policies for your robot in its final mass configuration.**

We recommend a **USB Tester 4-28V 7A LCD USB A&C Voltage Current Power Tester Multimeter** so you can evaluate the average and peak power draw for all the different sensors. Here are some example values:
 
**USB Bus A** 
USB-A Power for RPLidare S2 Laserscan - Operating Current: 40mA(5V power supply, in sleep); 400mA(5V power supply, working)
USB-A Microphone and Speaker ADC and DAQ - time sensitive - no power specs public but < 0.5 A - might be a lot lower - need to measure
USB-A Widefield Camera - cable way too long - normal video data rates - USB powered 5V Working Current: MAX 300mA

**USB Bus B** 
USB-C from RealSense - cable generally too long and and ends in wrong plug - ~700 mA - USB 3.1 needed
USB-A Data for Laserscan - 0 mA data only line - need to confirm
USB-A Display power and cap data - length ok - assume 0.5A power draw due to back lighting - no idea - could be lower?

Note that both of these buses are overloaded and out of spec, suggesting use of a powered USB hub. 
USB Bus A: 0.4 + 0.3 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).
USB Bus B: 0.7 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).

## Display Unit ("Face")

| Name | Quantity | Fab | Link | Picture |
|:------|:---:|----------|----------|-----|
| Face Frame                             | 1 | 3D printed | STL file goes here | picture |
| Frame Back (Unitree Go2, LimX Tron 1)  | 1 | 3D printed | STL file goes here | picture |
| Frame Back (Unitree G1)                | 1 | 3D printed | STL file goes here | picture |
| Widefield Camera Box                   | 1 | 3D printed | STL file goes here | picture |

**1 ea. Flexible HDMI to HDMI Cable**<br>
Twozoh Flexible HDMI to HDMI Cable Right Angled 90° 1FT<br>
Ultra Thin and Slim HDMI Cord Support 3D/4K@60Hz<br>
**For Unitree G1 and Go2**: 1FT length: https://www.amazon.com/dp/B09XHYH4KY<br>
**For Tron 1**: 3.3FT length: https://www.amazon.com/dp/B09XHZD6Z2<br>

**1 ea. Fisheye RGB Camera**<br>
Arducam 1080P Low Light WDR Ultra Wide Angle USB Camera Module<br>
2MP CMOS IMX291 160 Degree Fisheye Mini UVC USB2.0<br>
SKU: B0202<br>
[Purchasing link](https://www.arducam.com/arducam-1080p-low-light-wdr-ultra-wide-angle-usb-camera-module-for-computer-2mp-cmos-imx291-160-degree-fisheye-mini-uvc-usb2-0-spy-webcam-board-with-microphone-3-3ft-cable-for-windows-linux-mac-os.html)<br>

**1 ea. RealSense Depth Camera (i435)**<br>
Intel RealSense Depth Camera D435i, Silver, <br>
1080p Video Capture Resolution (82635D435IDK5P)<br>
https://www.amazon.com/Intel-RealSense-Depth-Camera-D435i/dp/B07MWR2YJB<br>

**1 ea. USB cable for RealSense**<br>
Short USB-C to USB-C Cable (1.5ft 2 Packs), 3.1 Gen 2 10Gbps 100W <br>
4K USBC Video High Speed Data Transfer Fast Charging Cord<br>
https://www.amazon.com/dp/B094V4RJGC<br>
NOTE: should be improved - should be a USB-C to USB-A cable<br>

**1 ea. High-Brightness Touch Screen**<br>
5inch High-Brightness Touch Screen, 1024x600 Pixels, <br>
Toughened Glass Panel, HDMI Interface, IPS Panel<br>
SKU: 27960<br>
Mfr. #: 5DP-CAPLCD-H<br>
Brand: Waveshare<br>
https://www.waveshare.com/5dp-caplcd.htm?sku=27960<br>

**1 ea. Touchscreen Power/USB cable**<br>
aceyoon 3 Pack 90 Degree USB C Cable <br>
0.6ft Short Right Angle Type C Charger Braided <br>
USBC to USB A 20cm Charging and Data Sync Cord<br>
https://www.amazon.com/dp/B096VYVR17<br>

**1 ea. Audio Amplifier**<br>
DROK 15W+15W 2.0 2pcs 12V Amplifier Board, Dual Channel Audio Amplifier Board <br>
PAM8620 DC 8-26V 24V Digital Stereo Amp Module Class D Mini Power <br>
https://www.amazon.com/dp/B0CQJRL235<br>

**2 ea. Speaker 42mm 8W 4ohm**<br>
Mouser #: 665-AS04204PR<br>
Mfr. #: AS04204PR<br>
Mfr.: PUI Audio<br>
https://mou.sr/4sO2Qsp<br>

**1 ea. Audio Cable**<br>
Seadream 3.5mm Aux Cable Short 2Pack <br>
8inch 3Port 3.5mm Right Angle Male to Male Stereo Audio Cable<br>
https://www.amazon.com/dp/B01L0YPVOY<br>

**1 ea. Sound Card ADC and DAC**
SABRENT USB External Stereo Sound Adapter 
USB-A (do not buy USB-C version - degraded audio quality)
https://www.amazon.com/dp/B00IRVQ0F8

**1 ea. Directional Microphone**
Comica Camera Microphone, CVM-VM10II 
Directional Microphone Cardioid Shotgun Video Camcorder Microphone
https://www.amazon.com/dp/B0748CYPDJ
Note: retain included 3.5 mm TRS cable; will be used in final assembly

**1 ea. Microphone Mount**
SMALLRIG Cold Shoe Mount Adapter with 1/4 Thread Hole – 1241
https://www.amazon.com/dp/B00HJFBUCQ

**5 ea. M3 Threaded Inserts for 3D Printing Components**
Many suppliers, for example:
Kadrick 520Pcs M2 M3 M4 M5 Threaded Inserts 
Assortment Kit for 3D Printing Components, 
Metric Brass Knurled Nuts, Insert by Heat into Plastic Parts
https://www.amazon.com/dp/B0D5V3TZLB

**5 ea. M3 x 8mm Thread Pitch Cap Screws**
Many suppliers, for example:
Iexcell 100 Pcs M3 x 8mm Thread Pitch 
0.5 mm Stainless Steel 304 
Hex Socket Button Head Cap Screws Bolts Kit
https://www.amazon.com/dp/B08H2HTTRT

## Face Mounting

| Robot  | Name | Quantity | Fab | Link | Picture |
|--------|------| --- |----------|----------|---------|
| Unitree Go2, LimX Tron 1 | Face Back | 1 | 3D printed | STL file goes here | picture |
| Unitree Go2, LimX Tron 1 | Face and Sensor Carrier ("Head") | 1 | 3D printed | STL file goes here | picture |
| Unitree G1 | Face Back | 1 | 3D printed | STL file goes here | picture |

### Unitree G1

**2 ea. M6 x 25mm Cap Screws** with nylon lock nut<br>
These are used to secure the frame back to the front of the Unitree G1<br> 

### Unitree Go2 and LimX Tron 1

**4 ea. M3 x 20mm Cap Screws** with nylon lock nuts and washers<br>
These are used to secure the frame back to the front of the standard sensor and display carrier ("head")<br>

## Thor Mounts

| Robot  | Name | Quantity | Fab | Link | Picture |
|--------|------| --- |----------|----------|---------|
| Unitree Go2 | Mount with sideplates | 1 | 3D printed | STL file goes here | picture |
| LimX Tron 1 | Head Mount | 1 | 3D printed | STL file goes here | picture |
| Unitree G1 | Mount with sideplates | 1 | 3D printed | STL file goes here | picture |

### LimX Tron 1

**1 ea. M5 T Slot Nut and Bolt Kit**<br> 
Many suppliers, for example:<br> 
200Pcs 2020 Aluminum Extrusion M5 T Slot Nuts and Bolts Screws<br>
20 Series Extruded Hardware Drop in T Nut Slide Nut<br>
M5x8 10mm for 20/20 80 20 2040 T V Slot Black Aluminum Profile Accessories<br>
https://www.amazon.com/dp/B08VGSNT2S<br>

### Unitree G1

**2 ea. Nylon Holding Strap**<br> 
Fastening Hook and Loop Cable Straps, 10 Pack <br> 
Black Self-Adhesive Cable Ties, Nylon Securing Straps with Buckles, <br> 
Adjustable and Reusable Cinch Straps for Cords Organized and Tidy(1" x 20")<br> 
https://www.amazon.com/dp/B088FJCJDL<br> 

**2 ea. M6 x 35mm Cap Screws**<br>
These are used to secure the TOP of the Thor mount.<br> 

**2 ea. M6 x 30mm Cap Screws**<br>
These are used to secure the BOTTOM of the Thor mount.<br>

### Unitree Go2

**1 ea. Nylon Holding Strap**<br>
Fastening Hook and Loop Cable Straps, 10 Pack<br>
Black Self-Adhesive Cable Ties, Nylon Securing Straps with Buckles<br>
Adjustable and Reusable Cinch Straps for Cords Organized and Tidy (1" x 20")<br>
https://www.amazon.com/dp/B088FJCJDL<br>

**2 ea. M3 x 35mm Cap Screws** with washers<br>
These are used to secure the FRONT of the Thor mount.<br>

**2 ea. M3 x 50mm Cap Screws** with washers<br>
These are used to secure the BACK of the Thor mount.<br> 

## Thor Power Cable Harness

Thor Power Cable
MICRO-FIT3.0 R-S 4 CIRCUIT 600MM
DigiKey Part No.: 900-2147561043-ND
Manufacturer Part No.: 2147561043
https://www.digikey.com/en/products/detail/molex/2147561043/12180337

## Power Electronics

| Robot  | Name |
|--------|------|
| All | MICRO-FIT3.0 R-S Thor Power Cable |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Black |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Red |
| All | Crimp butt connectors, heat shrink, associated tooling |
| Unitree Go2 and G1 | Male XT30 connector |
| Unitree Go2 | MATEKSYS BEC 12S Pro Synchronous switching step-down (buck) regulator | 
| Tron 1 | Male XT60 connector with wire leads |
| Unitree G1 | Male EC5 connector with 14AWG wire leeds |
| Unitree G1 | 120S 14.8V 10000 mAh LiPo battery with female EC5 connector and LiPo charger |
| Unitree G1 | CAMWAY 5PCS 2in1 1-8s Lipo Battery Low Voltage Buzzer Alarm |

### Tron 1 Custom Power Cable

The Tron 1 provides 24V through an XT60 jack. The Tron 1 does not need a power converter to power the audio amplifier or the Thor. Use crimp butt connectors to connect the male XT60 plug to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input to the audio amplifier. **You will damage either the audio amplifier, the Thor, or the robot, or all three, if you get this wrong. Do not reverse the polarity!**  

### Unitree G1 Custom Power Cable

The Unitree G1 **does not** provide sufficient power for the both the Thor and the audio amplifier. Therefore, an external LiPo battery is needed to power the Thor and the G1 just powers the audio amplifier via the G1's 24V/5A plug.

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to the audio amplifier cables (red, black) from the face unit. Plug the XT30 plug into the **MIDDLE** G1 power supply, which provides 24V/5A. **You will damage either the audio amplifier, or the robot, or both, if you get this wrong. Do not reverse the polarity!** 

2. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a Male EC5 connector to the MICRO-FIT3.0 R-S Thor power connector. This connector has 4 wires, two of which will be used for ground, and two of which will be used for 14.8V. Consult the Thor technical documentation to decide the correct wiring. **You will damage the Thor if you get this wrong. Do not reverse the polarity!** 

3. Connect the _Lipo Battery Low Voltage Buzzer Alarm_ to the balance port of the LiPo battery to avoid damaging the LiPo battery due to overdischarge. Use the second velcro nylon strap to attach the LiPo battery to the Thor mount.

### Unitree Go2 Custom Power Cable

The Unitree Go2 provides 28 to 33.6V, which is too much for the Audio Amplifier. Solution - use an MATEKSYS BEC 12S Pro Synchronous switching step-down (buck) regulator to provide 12V to the audio amplifier. 

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input to the MATEKSYS BEC 12S power. Add a drop of solder to short the 12V config pins of the MATEKSYS BEC 12S so that is provides 12V rather than the default 5.2V. Connect the outputs of the MATEKSYS BEC 12S to the red/black wires from the audio amplifier in the face unit. **You will damage either the audio amplifier, or the Thor, or the robot, or all three, if you get this wrong. Do not reverse the polarity!** 

2. Plug the XT30 plug into the 33.6V Go2 power supply port. 



### Display

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link | Picture |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|:---------:|
| Elecrow 800x400 Touchscreen Display | RC050 | 1 | Electronics | 3rd party | | https://www.amazon.com/ELECROW-Raspberry-Touchscreen-Monitor-HDMI-Compatible/dp/B07FDYXPT7 | |
| MicroUSB cable for display power | 200017-BLKx2 | 1 | Cabling | 3rd party | Cable from this pack also used for RPLidar connection | https://www.amazon.com/Cable-Matters-Combo-Pack-Right-Inches/dp/B00S8GU03A | |
| HDMI cable for display | HD-016-0.3M-L | 1 | Cabling | 3rd party | | 90 Deg connector, Twozoh Flexible HDMI to HDMI Cable Left Angled 90° 1FT, Ultra Thin and Slim HDMI Cord Support 3D/4K@60Hz. https://www.amazon.com/dp/B09XHZB9X5 | |
| HDMI to DP adapter | 5e40d1e3-7769-4fd2-8da5-d54d582f8e3b | 1 | Adapter | 3rd party | | Displayport to HDMI Adapter 4K 24K Gold Plated Displayport DP to HDMI Female Converter. https://www.amazon.com/dp/B09MTKHFKR | |

## Laserscan/LIDAR

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link | Picture |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|:---------:|
| RPlidar 2d Lidar | RPLIDAR A1M8 | 1 | Electronics | 3rd party | Legs are unscrewed and then the unit is mounted on top of the lidar mount. | https://www.amazon.com/Slamtec-RPLIDAR-Scanning-Avoidance-Navigation/dp/B07TJW5SXF | |
| MicroUSB bridge connector for RPlidar | | 1 | Cabling | 3rd party | | https://www.amazon.com/Cable-Matters-Combo-Pack-Right-Inches/dp/B00S8GU03A | |

## Webcam/microphone

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link | Picture |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|:---------:|
| Logitech Brio Webcam | 960-001589 | 1 | Electronics | 3rd party | Webcam is glued into bezel, and the USB cable is shortened via a USB-A connector. | https://www.amazon.com/Logitech-Webcam-Meetings-Streaming-Built/dp/B0BXGFFSL1 | |
| Webcam USB-A jack | | | Cabling | Custom Fab | USB end for the shortened webcam cable to be plugged into the USB A port on the hub. | Maxmoral 10PCS USB 2.0 Connector A Type Male 4-Pin Plug with Black Plastic Cover DIY Connector. https://www.amazon.com/dp/B081YV9VDH | |

## USB HUB

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link | Picture |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|:---------:|
| Coolgear powered USB Hub | CG-U3MINI4PH | 1 | Electronics | 3rd party | Enclosure is removed and discarded. | https://www.amazon.com/Coolgear-Powered-Port-Surge-Protection/dp/B07G7GP15C/ref=sr_1_4?s=electronics | |
| USB C to USB B 3.0 Cable | 201007-BLK-0.3m | 1 | Cabling | 3rd party | This must be a USB 3.0 cable otherwise the system does not work | https://www.amazon.com/Cable-Matters-Short-USB-3-0/dp/B0DN4NWJ9D | |
| Powered USB hub power cable (Barrel Jack to JST) | | 1 | Cabling | Custom Fab | Uses the barrel jack from the coolgear kit, butt connectors, and JST cables/plug | | |

## Depth Camera

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link | Picture |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|:---------:|
| Intel D435i depth camera | 82635D435IDK5P | 1 | electronics | 3rd party | Uses cable that comes with the Unitree. Also uses a USB-C to USB-A adapter | | |
| Unitree 435 mount and cable | | 1 | mount/cable | 3rd party | Comes with each Go2 EDU, but we pay extra for it | | |
| USB-C to USB-A adapter | US701 | 1 | connector | 3rd party | For connecting the d435i to the Jetson AGX | https://www.amazon.com/UGREEN-Adapter-10Gbps-Converter-Samsung/dp/B0CY1Y3TSQ/ref=sr_1_4?s=electronics | |



## Backpack Unit

| Name | Part No. | Quantity | Category | Fab | Build Notes | Link |
|:------:|:-------------:|:----------:|:----------:|:-----:|:-------------:|:------:|
| Shell | | 1 | Housing | 3D printed | | <STL file goes here> |
| Base Mount bracket | | 1 | Housing | 3D printed | | <STL file goes here> |
| Lid | | 1 | Housing | 3D printed | | <STL file goes here> |
| AGX push fit bracket | | 1 | Housing | 3D printed | | <STL file goes here> |
| Magnets for snap on lid | | 4 | Housing | 3rd party | | |
| Openmind Powerboard | | 2 | Electronics | Custom Fab | Openmind PCB | |
| Nvidia Jetson AGX Orin Developer Kit | ‎945-13730-0050-000 | 1 | Electronics | 3rd party | | https://www.amazon.com/NVIDIA-Jetson-Orin-64GB-Developer/dp/B0BYGB3WV4/ref=sr_1_2?s=electronics |
| Waveshare Audio codec driver | ‎RS232/485 USB All | 1 | Electronics | 3rd party | USB drive enclosure is removed and discarded. | https://www.amazon.com/Waveshare-USB-Converter-Raspberry-Driver-Free/dp/B08R38TXXL |
| Speakers | a19090500ux0199 | 2 | Electronics | 3rd party | +ve/-ve leads soldered to JST 4 pin adapter | https://www.amazon.com/uxcell-Internal-Magnet-Speaker-Loudspeaker/dp/B082ZPP56D |
| Speaker cable (custom) | | 1 | Cabling | Custom Fab | Modified from cable that is shipped with the Waveshare Audio speaker system | |
| Ethernet bridge | SPM10236514602 | 1 | Electronics | 3rd party | Need to remove (and discard) enclosure | https://www.amazon.com/dp/B0D9BN22ZX |
| USB C to JST power connector for the Ethernet board | | 1 | Cabling | Custom Fab | | |
| 2.1 mm Male Barrel Jack power in cable | | 1 | Cabling | Custom Fab | | |
| 2.1 mm Female Barrel Jack power out cable | | 1 | Cabling | Custom Fab | | |
| Split power delivery cable | | 1 | Cabling | Custom Fab | | |
| 25 mm M3 socket head screw with washer for front 2 holes of interface bracket | | 2 | Screws | 3rd party | The SHORT screw are used near the head of the dog | |
| 35 mm M3 socket head screw with washer for back 2 holes of interface bracket | | 2 | Screws | 3rd party | The LONGer M3 bolts are used near the tail of the dog | |
