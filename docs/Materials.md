<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->
- [1. Safety](#safety)
   * [1.1 DANGER: Power Budget and Thermal Limits](#danger-power-budget-and-thermal-limits)
   * [1.2 DANGER: Robot Stability](#danger-robot-stability)
- [2. Materials](#materials)
   * [2.1 Display Unit ("Face")](#display-unit-face)
   * [2.2 Face and Sensor Carrier ("Head"); LiDAR](#face-mounting)
      + [Unitree G1](#unitree-g1)
      + [Unitree Go2 and LimX Tron 1](#unitree-go2-and-limx-tron-1)
   * [2.3 Thor Mounts](#thor-mounts)
      + [LimX Tron 1](#limx-tron-1)
      + [Unitree G1](#unitree-g1-1)
      + [Unitree Go2](#unitree-go2)
- [3. Cables and Power](#cables-and-power)
   * [3.1 Thor Power Harness](#thor-power-harness)
   * [3.2 Power Electronics](#power-electronics)
      + [Tron 1 Custom Power Cable](#tron-1-custom-power-cable)
      + [Unitree G1 Custom Power Cable](#unitree-g1-custom-power-cable)
      + [Unitree Go2 Custom Power Cable](#unitree-go2-custom-power-cable)
   * [3.3 Example BrainPack Power Budget Calculation](#example-brainpack-power-budget-calculation)
   * [3.4 Powered USB Hubs](#powered-usb-hubs)
<!-- TOC end -->

<!-- TOC --><a name="brainpack"></a>
# BrainPack

<!-- TOC --><a name="brainpack"></a>
## 1. Safety

<!-- TOC --><a name="danger-power-budget-and-thermal-limits"></a>
### 1.1 DANGER: Power Budget and Thermal Limits

**It is easy to operate a robot above its design power budget. For safe use, you must carefully consider the robot's intended use, average and peak power requirements, the robot's physical environment (e.g. external air temperature), and the power/thermal interplay of simultaneous movement, sensing, and compute.** 

Unless you get this right, you may experience fast battery drain, intermittent faults and resets, electrical shorts and fires, overheating, poor sensor performance and many other possible problems. 

**Example 1**: when a robot tries to speak (at max volume) and walk at the same time, while also running multiple large policies, this could overload (and reset) the power system. The humanoid will then suddenly crash to the floor. Testing individual robot subsystems will not predict this problem, which only occurs when the robot wishes to move, think, and speak at the same time.

**Potential Solution**: use an inline **USB Voltage Current Power Tester Multimeter** (such as the [FNB58USB Voltage/Current/Power tester/monitor](https://www.fnirsi.com/products/fnb58)) to measure the actual power draw of your sensors and other electronics payload. If needed, change how you are powering your computers and sensors, such as by moving loads to other power buses, providing powered USB hubs, or adding external batteries (but see [below](#danger-robot-stability)).

**Example 2**: The robot performs flawlessly in an air conditioned lab, but falls over frequently when deployed in a hot sunny environment. In this case, different joint are probably overheating, switching the system to emergency damp mode, resulting in a fall and damage to the robot. 

**Potential Solution**: ensure that your software is monitoring the temperature and currents of all joints. If your software detects operation near the thermal limits, warn bystanders and perform a safe sink-to-floor action with an audible alarm and flashing light alarm.   

<!-- TOC --><a name="danger-robot-stability"></a>
### 1.2 DANGER: Robot Stability

**CAUTION: adding extra mass (such as external computers, sensors, grippers, and batteries) to the robot will affect your motion policies and the robot's stability and ability to navigate terrain. You may for example observe the robot swaying back and forth while simply trying to stand.**

**Potential Solution**: train custom motion policies for your robot in its final mass configuration.

<!-- TOC --><a name="materials"></a>
## 2. Materials

<!-- TOC --><a name="display-unit-face"></a>
### 2.1 Display Unit ("Face")

| Name | Quantity | Fab | Link | Picture |
|:------|:---:|----------|----------|-----|
| Face Frame                            | 1 | 3D printed | STL file goes here | picture |
| Face Back (Unitree Go2, LimX Tron 1)  | 1 | 3D printed | STL file goes here | picture |
| Face Back (Unitree G1)                | 1 | 3D printed | STL file goes here | picture |
| Widefield Camera Box                  | 1 | 3D printed | STL file goes here | picture |

**<ins>1 ea. Flexible HDMI to HDMI Cable</ins>** This is used to connect the Thor to the LCD screen. Suggested part: Twozoh Flexible HDMI to HDMI Cable Right Angled 90° 1FT Ultra Thin and Slim HDMI Cord Support 3D/4K@60Hz
- For Unitree G1 and Go2: 1FT length: https://www.amazon.com/dp/B09XHYH4KY
- For Tron 1: 3.3FT length: https://www.amazon.com/dp/B09XHZD6Z2

**<ins>1 ea. Fisheye RGB Camera</ins>** Suggested part: Arducam 1080P Low Light WDR Ultra Wide Angle USB Camera Module 2MP CMOS IMX291 160 Degree Fisheye Mini UVC USB2.0 SKU: B0202 [Purchasing link](https://www.arducam.com/arducam-1080p-low-light-wdr-ultra-wide-angle-usb-camera-module-for-computer-2mp-cmos-imx291-160-degree-fisheye-mini-uvc-usb2-0-spy-webcam-board-with-microphone-3-3ft-cable-for-windows-linux-mac-os.html)

**<ins>1 ea. RealSense Depth Camera (i435)</ins>** Intel RealSense Depth Camera D435i, Silver 1080p Video Capture Resolution (82635D435IDK5P) https://www.amazon.com/Intel-RealSense-Depth-Camera-D435i/dp/B07MWR2YJB

**<ins>1 ea. USB Cable for RealSense</ins>** Suggested part: Short USB-C to USB-C Cable (1.5ft 2 Packs), 3.1 Gen 2 10Gbps 100W 4K USBC Video High Speed Data Transfer Fast Charging Cord https://www.amazon.com/dp/B094V4RJGC **Design notes**: should be improved - should be a USB-C to USB-A cable

**<ins>1 ea. High-Brightness Touch Screen</ins>** 5 inch High-Brightness Touch Screen, 1024x600 Pixels Toughened Glass Panel, HDMI Interface, IPS Panel SKU: 27960 Mfr. #: 5DP-CAPLCD-H Brand: Waveshare https://www.waveshare.com/5dp-caplcd.htm?sku=27960

**<ins>1 ea. Touchscreen Power/USB Cable</ins>** Suggested part: Aceyoon 90 Degree USB C Cable 0.6ft Short Right Angle Type C https://www.amazon.com/dp/B096VYVR17

**<ins>1 ea. Audio Amplifier</ins>** DROK 15W+15W 2.0 2pcs 12V Amplifier Board, Dual Channel Audio Amplifier Board PAM8620 DC 8-26V Digital Stereo Amp Module Class D Mini Power https://www.amazon.com/dp/B0CQJRL235 **Design notes**: Working voltage: DC8~26V, 15W stereo (24V 8ohm)/ 10W stereo (12V 8 ohm), if connect 4 ohm or 2 ohm speaker, the power will be automatically limited to 15W. Calculation: We are powering with 12V. Assuming auto limiting to 15W per side, aka (12V/15W =) 1.25 A per channel, the combined max power draw is limited to 1.25 + 1.25 = 2.5A, with overhead that works out to ~3A. 

**<ins>2 ea. Speaker 42mm 8W 4ohm</ins>** Mouser #: 665-AS04204PR Mfr. #: AS04204PR Mfr.: PUI Audio https://mou.sr/4sO2Qsp. These are 4 ohm speakers. The DROK audio amplifier will auto limit power to 15W per side (which overloads the speakers, leading to distortion, so do not turn the volume up all the way). 

**<ins>1 ea. Audio Cable</ins>** Seadream 3.5mm Aux Cable Short 2Pack 8 inch 3Port 3.5mm Right Angle Male to Male Stereo Audio Cable https://www.amazon.com/dp/B01L0YPVOY

**<ins>1 ea. Sound Card ADC and DAC</ins>** SABRENT USB External Stereo Sound Adapter USB-A (do not buy USB-C version - degraded audio quality) https://www.amazon.com/dp/B00IRVQ0F8

**<ins>1 ea. Directional Microphone</ins>** Comica Camera Microphone, CVM-VM10II Directional Microphone Cardioid Shotgun Video Camcorder Microphone https://www.amazon.com/dp/B0748CYPDJ **Design notes**: retain included 3.5 mm TRS cable; will be used in final assembly

**<ins>1 ea. Microphone Mount** SMALLRIG Cold Shoe Mount Adapter with 1/4 Thread Hole – 1241 https://www.amazon.com/dp/B00HJFBUCQ

**<ins>5 ea. M3 Threaded Inserts for 3D Printing Components</ins>** Many suppliers, for example: Kadrick 520Pcs M2 M3 M4 M5 Threaded Inserts Assortment Kit for 3D Printing Components Metric Brass Knurled Nuts https://www.amazon.com/dp/B0D5V3TZLB

**<ins>5 ea. M3 x 8mm Thread Pitch Cap Screws</ins>** Many suppliers, for example: Iexcell 100 Pcs M3 x 8mm Thread Pitch 0.5 mm Stainless Steel 304 Hex Socket Button Head Cap Screws Bolts Kit https://www.amazon.com/dp/B08H2HTTRT

<!-- TOC --><a name="face-mounting"></a>
### 2.2 Face and Sensor Carrier ("Head"); LiDAR

| Robot  | Name | Quantity | Fab | Link | Picture |
|--------|------| --- |----------|----------|---------|
| Unitree G1               | Face Back | 1 | 3D printed | STL file goes here | picture |
| Unitree Go2, LimX Tron 1 | Face Back | 1 | 3D printed | STL file goes here | picture |
| Unitree Go2, LimX Tron 1 | Face and Sensor Carrier ("Head") | 1 | 3D printed | STL file goes here | picture |
| Unitree Go2, LimX Tron 1 | Face and Sensor Carrier, Lid | 1 | 3D printed | STL file goes here | picture |

<!-- TOC --><a name="unitree-g1"></a>
#### Unitree G1

**2 ea. M6 x 25mm Cap Screws** with nylon lock nut. Generic part, many suppliers. These are used to secure the face back to the front of the Unitree G1.

The Unitree G1 is supplied with an internal [Livox Mid360](https://www.livoxtech.com/mid-360). Please refer to the Unitree and Livox documentation.  

<!-- TOC --><a name="unitree-go2-and-limx-tron-1"></a>
#### Unitree Go2 and LimX Tron 1

**4 ea. M3 x 20mm Cap Screws** with nylon lock nuts and washers. Generic part, many suppliers. These are used to secure the face back to the front of the **Face and Sensor Carrier ("Head")**.

**1 ea. RPLidar S2 - ToF LiDAR** 360 Degree Laser Range Scanner, 2D, 30-meter range, sunlight resistant, 10Hz (600rpm), 32kHz sample rate (angular resolution is 0.1125°). https://www.slamtec.com/en/s2

Once all the electronics/wiring has been completed, close the head with the lid. The lid also serves as the base of the [RPLidar S2 - ToF LiDAR](https://www.slamtec.com/en/s2). 

<!-- TOC --><a name="thor-mounts"></a>
### 2.3 Thor Mounts

| Robot  | Name | Quantity | Fab | Link | Picture |
|--------|------| --- |----------|----------|---------|
| Unitree G1  | Mount with sideplates | 1 | 3D printed | STL file goes here | picture |
| Unitree Go2 | Mount with sideplates | 1 | 3D printed | STL file goes here | picture |
| LimX Tron 1 | Head Mount | 1 | 3D printed | STL file goes here | picture |

<!-- TOC --><a name="limx-tron-1"></a>
#### LimX Tron 1

**1 ea. M5 T Slot Nut and Bolt Kit** Many suppliers, for example: 200Pcs 2020 Aluminum Extrusion M5 T Slot Nuts and Bolts Screws 20 Series Extruded Hardware Drop in T Nut Slide Nut M5x8 10mm for 20/20 80 20 2040 T V Slot Black Aluminum Profile Accessories https://www.amazon.com/dp/B08VGSNT2S

<!-- TOC --><a name="unitree-g1-1"></a>
#### Unitree G1

**2 ea. Nylon Holding Strap** Fastening Hook and Loop Cable Straps, 10 Pack Black Self-Adhesive Cable Ties, Nylon Securing Straps with Buckles Adjustable and Reusable Cinch Straps for Cords Organized and Tidy(1" x 20") https://www.amazon.com/dp/B088FJCJDL

**2 ea. M6 x 35mm Cap Screws** Generic part, many suppliers. These are used to secure the TOP of the Thor mount. 

**2 ea. M6 x 30mm Cap Screws** Generic part, many suppliers. These are used to secure the BOTTOM of the Thor mount.

<!-- TOC --><a name="unitree-go2"></a>
#### Unitree Go2

**1 ea. Nylon Holding Strap** Fastening Hook and Loop Cable Straps, 10 Pack Black Self-Adhesive Cable Ties, Nylon Securing Straps with Buckles Adjustable and Reusable Cinch Straps for Cords Organized and Tidy (1" x 20") https://www.amazon.com/dp/B088FJCJDL

**2 ea. M3 x 35mm Cap Screws** with washers. Generic part, many suppliers. These are used to secure the FRONT of the Thor mount.

**2 ea. M3 x 50mm Cap Screws** with washers. Generic part, many suppliers. These are used to secure the BACK of the Thor mount. 

<!-- TOC --><a name="cables-and-power"></a>
## 3. Cables and Power

The Nvidia Thor is typically powered with:

* 4S 14.8V external LiPo (Unitree G1)
* 28V to 33.6V main robot power bus (Unitree Go2)
* 24V main robot power bus (LimX Tron 1)

The different robots have different power plugs:

* Unitree G1 - 24V/5A plug - can be used for the audio amplifier directly (which accepts anything below 26V)
* Tron 1 - 24V via XT60 plug - can be used for the audio amplifier directly (which accepts anything below 26V) **AND** the Nvidia Thor
* Unitree Go2 - 28V to 33.6V via XT30 - can be used for the Nvidia Thor **AND** via a step-down (buck) regulator, the audio amplifier.

**NOTE: In general, you will need to design, fabricate, and assemble a custom step-down regulator which (1) takes 24 to 34V and (2) provides 12-17V for the audio amplifier, and 5V 2A for the LCD screen back-lighting. In an emergency, you can use 2 ea. MATEKSYS BEC 12S Pro Synchronous switching step-down regulators, or equivalent, but this is probably not ideal.**

<!-- TOC --><a name="thor-power-harness"></a>
### 3.1 Thor Power Harness

Thor Power Cable, MICRO-FIT3.0 R-S 4 CIRCUIT 600MM<br>
DigiKey Part No.: 900-2147561043-ND<br>
Manufacturer Part No.: 2147561043<br>
https://www.digikey.com/en/products/detail/molex/2147561043/12180337<br>

<!-- TOC --><a name="power-electronics"></a>
### 3.2 Power Electronics

| Robot  | Name |
|--------|------|
| All | MICRO-FIT3.0 R-S Thor Power Cable |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Black |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Red |
| All | Crimp butt connectors, heat shrink, associated tooling |
| Unitree Go2 and G1 | Male XT30 connector with wire leads |
| Unitree Go2 | MATEKSYS BEC 12S Pro 9-55V to 5/8/12V-5A Synchronous switching step-down (buck) regulator | 
| Tron 1 | Male XT60 connector with wire leads |
| Unitree G1 | Male EC5 connector with 14AWG wire leads |
| Unitree G1 | 120S 14.8V 10000 mAh LiPo battery with female EC5 connector and LiPo charger |
| Unitree G1 | CAMWAY 5PCS 2 in 1 1-8s LiPo Battery Low Voltage Buzzer Alarm |

<!-- TOC --><a name="tron-1-custom-power-cable"></a>
#### LimX Tron 1 Custom Power Cable

The Tron 1 provides 24V through an XT60 jack. The Tron 1 does not need a power converter to power the audio amplifier or the Thor. Use crimp butt connectors to connect the male XT60 plug to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input to the audio amplifier. **You will damage the audio amplifier, the Thor, the robot, or all three, if you get this wrong. Do not reverse the polarity!**  

<!-- TOC --><a name="unitree-g1-custom-power-cable"></a>
#### Unitree G1 Custom Power Cable

The Unitree G1 **does not** provide sufficient power for the both the Thor and the audio amplifier. Therefore, an external LiPo battery is needed to power the Thor. The G1 just powers the audio amplifier via the G1's 24V/5A plug. **WARNING: Do not plug in the XT30 connector into the G1's 5V or 55V connectors. The 24V connector is the one in the middle.**

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to the audio amplifier cables (red, black) from the face unit. Plug the XT30 plug into the **MIDDLE** G1 power supply, which provides 24V/5A. **You will the audio amplifier, the G1, or both, if you get this wrong. Do not reverse the polarity!** 

2. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a Male EC5 connector to the MICRO-FIT3.0 R-S Thor power connector. This connector has 4 wires, two of which will be used for ground, and two of which will be used for 14.8V. Consult the Thor technical documentation to determine the correct wiring. **You will damage the Thor if you get this wrong. Do not reverse the polarity!** **WARNING FIRE HAZARD: Do not short the 120S 14.8V 10000 mAh LiPo battery!**  

3. Use the second Velcro nylon strap to attach the LiPo battery to the Thor mount. Connect the _Lipo Battery Low Voltage Buzzer Alarm_ to the balance port of the LiPo battery to avoid damaging the LiPo battery due to over-discharge. **WARNING BATTERY DAMAGE: Do not fully drain the LiPo battery. The Thor will try to drain the battery to below 12V, which will destroy it. Replace the battery when it has discharged to about 14V.**

<!-- TOC --><a name="unitree-go2-custom-power-cable"></a>
#### Unitree Go2 Custom Power Cable

The Unitree Go2 provides 28 to 33.6V, which is too much for the audio amplifier. Solution: use an MATEKSYS BEC 12S Pro Synchronous switching step-down (buck) regulator to provide 12V to the audio amplifier. 

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input of the MATEKSYS BEC 12S power buck. Add a drop of solder to short the 12V config pins of the MATEKSYS BEC 12S so that it provides 12V rather than the default 5.2V. Connect the outputs of the MATEKSYS BEC 12S to the red/black wires from the audio amplifier in the face unit. **You will damage the audio amplifier, the Thor, or the robot, or all three, if you get this wrong. Do not reverse the polarity!** 

2. Plug the XT30 plug into the 33.6V Go2 power supply port. 

<!-- TOC --><a name="example-brainpack-power-budget-calculation"></a>
### 3.3 Example BrainPack Power Budget Calculation

We recommend a [FNB58USB Voltage/Current/Power tester/monitor](https://www.fnirsi.com/products/fnb58) to measure actual power draw.

**USB Bus A** This must be externally powered!<br>
USB-A Power for RPLidar S2 Laserscan - Operating Current: 40mA (5V power supply, in sleep); 400mA (5V power supply, working); actual 340mA<br>
USB-A Data for RPLidar S2 Laserscan - 40 mA<br>
USB-A Microphone and Speaker ADC and DAQ - time sensitive data - Microphone only with Comica 24 mA<br>
USB-A LCD Display power - sleep 130mA to full power 900mA depending on back-lighting<br>

**USB Bus B** This should be externally powered!<br>
USB-C RealSense - peak 700 mA - USB 3.1 critical - 60mA sleep, 130mA RGB only<br>
USB-A Widefield Camera - normal video data rates - USB 2.0 ok - actual 210mA<br>

<!-- TOC --><a name="powered-usb-hubs"></a>
### 3.4 Powered USB Hubs

For reliable and stable performance, **you must use powered USB hubs**. We recommend the Coolgear 3.2 Gen 1 USB Hub - 4 Port USB Hub with 5Gbps Data Transfers, Mountable Metal Housing, 5V Power Adapter, ESD Surge Protection, Bus or Self Powered https://www.amazon.com/dp/B07G7GP15C. 

This hub can provide 20W total power, or 900 mA per port. Provide 5V via the barrel jack connector; you can obtain 5V via a MATEKSYS BEC 12S (or equivalent). The MATEKSYS BEC 12S can provide Continuous 5A output Peak 9A output. 
