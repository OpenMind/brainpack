<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->
- [Cables and Power](#cables-and-power)
   * [Thor Power Cable Harness](#thor-power-cable-harness)
   * [Power Electronics](#power-electronics)
      + [Tron 1 Custom Power Cable](#tron-1-custom-power-cable)
      + [Unitree G1 Custom Power Cable](#unitree-g1-custom-power-cable)
      + [Unitree Go2 Custom Power Cable](#unitree-go2-custom-power-cable)
   * [Example BrainPack Power Budget Calculation ](#example-brainpack-power-budget-calculation)
<!-- TOC end -->

<!-- TOC --><a name="cables-and-power"></a>
# Cables and Power
[//]:# (**v 0.2**)

<!-- TOC --><a name="thor-power-cable-harness"></a>
## Thor Power Cable Harness

Thor Power Cable<br>
MICRO-FIT3.0 R-S 4 CIRCUIT 600MM<br>
DigiKey Part No.: 900-2147561043-ND<br>
Manufacturer Part No.: 2147561043<br>
https://www.digikey.com/en/products/detail/molex/2147561043/12180337<br>

<!-- TOC --><a name="power-electronics"></a>
## Power Electronics

| Robot  | Name |
|--------|------|
| All | MICRO-FIT3.0 R-S Thor Power Cable |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Black |
| All | Mil-spec hookup wire, M22759/16-20 Mil-Spec Tefzel Hi-Temp Stranded Wire 20AWG Gauge, Red |
| All | Crimp butt connectors, heat shrink, associated tooling |
| Unitree Go2 and G1 | Male XT30 connector with wire leads |
| Unitree Go2 | MATEKSYS BEC 12S Pro Synchronous switching step-down (buck) regulator | 
| Tron 1 | Male XT60 connector with wire leads |
| Unitree G1 | Male EC5 connector with 14AWG wire leads |
| Unitree G1 | 120S 14.8V 10000 mAh LiPo battery with female EC5 connector and LiPo charger |
| Unitree G1 | CAMWAY 5PCS 2in1 1-8s LiPo Battery Low Voltage Buzzer Alarm |

<!-- TOC --><a name="tron-1-custom-power-cable"></a>
### Tron 1 Custom Power Cable

The Tron 1 provides 24V through an XT60 jack. The Tron 1 does not need a power converter to power the audio amplifier or the Thor. Use crimp butt connectors to connect the male XT60 plug to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input to the audio amplifier. **You will damage either the audio amplifier, the Thor, the robot, or all three, if you get this wrong. Do not reverse the polarity!**  

<!-- TOC --><a name="unitree-g1-custom-power-cable"></a>
### Unitree G1 Custom Power Cable

The Unitree G1 **does not** provide sufficient power for the both the Thor and the audio amplifier. Therefore, an external LiPo battery is needed to power the Thor and the G1 just powers the audio amplifier via the G1's 24V/5A plug.

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to the audio amplifier cables (red, black) from the face unit. Plug the XT30 plug into the **MIDDLE** G1 power supply, which provides 24V/5A. **You will the audio amplifier, the G1, or both, if you get this wrong. Do not reverse the polarity!** 

2. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a Male EC5 connector to the MICRO-FIT3.0 R-S Thor power connector. This connector has 4 wires, two of which will be used for ground, and two of which will be used for 14.8V. Consult the Thor technical documentation to determine the correct wiring. **You will damage the Thor if you get this wrong. Do not reverse the polarity!** 

3. Use the second velcro nylon strap to attach the LiPo battery to the Thor mount. Connect the _Lipo Battery Low Voltage Buzzer Alarm_ to the balance port of the LiPo battery to avoid damaging the LiPo battery due to over-discharge. 

<!-- TOC --><a name="unitree-go2-custom-power-cable"></a>
### Unitree Go2 Custom Power Cable

The Unitree Go2 provides 28 to 33.6V, which is too much for the audio amplifier. Solution: use an MATEKSYS BEC 12S Pro Synchronous switching step-down (buck) regulator to provide 12V to the audio amplifier. 

1. Connect (using crimp butt connectors, cover with mil-spec glue coated heat shrink) a male XT30 connector to **BOTH** the MICRO-FIT3.0 (for the Thor) and the power input to the MATEKSYS BEC 12S power. Add a drop of solder to short the 12V config pins of the MATEKSYS BEC 12S so that is provides 12V rather than the default 5.2V. Connect the outputs of the MATEKSYS BEC 12S to the red/black wires from the audio amplifier in the face unit. **You will damage the audio amplifier, the Thor, or the robot, or all three, if you get this wrong. Do not reverse the polarity!** 

2. Plug the XT30 plug into the 33.6V Go2 power supply port. 

<!-- TOC --><a name="example-brainpack-power-budget-calculation"></a>
## Example BrainPack Power Budget Calculation 

**USB Bus A**<br>
USB-A Power for RPLidar S2 Laserscan - Operating Current: 40mA (5V power supply, in sleep); 400mA (5V power supply, working)<br>
USB-A Microphone and Speaker ADC and DAQ - time sensitive data - peak 0.5 A<br>
USB-A Widefield Camera - normal video data rates - peak 300mA<br>

**USB Bus B**<br>
USB-C from RealSense - peak 700 mA - USB 3.1 critical<br>
USB-A Data for RPLidar S2 Laserscan - 0 mA<br>
USB-A LCD Display power - peak 500mA depending on back-lighting<br>

Note that both of these buses would be overloaded and out of spec, suggesting use of a powered USB hub.<br> 
USB Bus A: 0.4 + 0.3 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).<br>
USB Bus B: 0.7 + 0.5 = 1.2A - which exceeds USB 3.0/3.1: 4.5W (5V @ 0.9A).<br>