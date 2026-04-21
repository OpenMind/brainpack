# Materials and Assembly
[//]:# (**v 0.2**)

# HAZARD/DANGER: Power Budget and Thermal Limits

**Be aware that regardless of robot, it is easy to operate it above its design power budget. For safe use, you must carefully consider the robot's intended use, average and peak power requirements, the robot's physical environment (e.g. air temperature), and the power/thermal interplay of simultaneous movement, sensing, and compute.** 

Unless you get this right, you may experience fast battery drain, intermittent faults and resets, electrical shorts and fires, overheating, poor sensor performance and many other possible problems. 

**Example 1**: when a robot tries to speak (at max volume) and walk at the same time, while also running multiple large policies, this could overload (and reset) the power system. The humanoid will then suddenly crash to the floor. Testing individual robot subsystems will not predict this problem, which only occurs when the robot wishes to move, think, and speak at the same time.

**Potential Solution**: use an inline **USB Voltage Current Power Tester Multimeter** to measure the actual power draw of your payload. If needed, change how you are powering your computers and sensors, such as by moving loads to other power buses or adding external batteries. 

**Example 2**: The robot performs flawlessly in an air conditioned lab, but falls over frequently when deployed in hot sunny environment. In this case, different joint are probably overheating, switching the system to damp mode, resulting in a fall and damage to the robot. 

**Potential Solution**: ensure that your software is monitoring the temperature and currents of all joints. If your software detects operation near the thermal limits, warn bystanders and perform a safe sink-to-floor action with audible and flashing light alarm.   

# HAZARD/DANGER: Robot Stability

**CAUTION/NOTE: adding extra mass to the robot will affect your motion policies and the robot's stability and ability to navigate terrain. Solution: train custom motion policies for your robot in its final mass configuration.**

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

## Example BrainPack Power Budget Calculation 

**USB Bus A** 
USB-A Power for RPLidar S2 Laserscan - Operating Current: 40mA (5V power supply, in sleep); 400mA (5V power supply, working)
USB-A Microphone and Speaker ADC and DAQ - time sensitive data - peak 0.5 A
USB-A Widefield Camera - normal video data rates - peak 300mA

**USB Bus B** 
USB-C from RealSense - peak 700 mA - USB 3.1 critical
USB-A Data lines for RPLidar S2 Laserscan - 0 mA data only line
USB-A LCD Display power - peak 500mA depending on back-lighting

Note that both of these buses would be overloaded and out of spec, suggesting use of a powered USB hub. 
USB Bus A: 0.4 + 0.3 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).
USB Bus B: 0.7 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).
