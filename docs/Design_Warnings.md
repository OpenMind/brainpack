<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->
- [Usage](#usage)
   * [DANGER: Power Budget and Thermal Limits](#danger-power-budget-and-thermal-limits)
   * [DANGER: Robot Stability](#danger-robot-stability)
<!-- TOC end -->

<!-- TOC --><a name="materials-and-assembly"></a>
# Usage
[//]:# (**v 0.2**)

<!-- TOC --><a name="danger-power-budget-and-thermal-limits"></a>
## DANGER: Power Budget and Thermal Limits

**It is easy to operate a robot above its design power budget. For safe use, you must carefully consider the robot's intended use, average and peak power requirements, the robot's physical environment (e.g. air temperature), and the power/thermal interplay of simultaneous movement, sensing, and compute.** 

Unless you get this right, you may experience fast battery drain, intermittent faults and resets, electrical shorts and fires, overheating, poor sensor performance and many other possible problems. 

**Example 1**: when a robot tries to speak (at max volume) and walk at the same time, while also running multiple large policies, this could overload (and reset) the power system. The humanoid will then suddenly crash to the floor. Testing individual robot subsystems will not predict this problem, which only occurs when the robot wishes to move, think, and speak at the same time.

**Potential Solution**: use an inline **USB Voltage Current Power Tester Multimeter** to measure the actual power draw of your payload. If needed, change how you are powering your computers and sensors, such as by moving loads to other power buses, providing powered USB hubs, or adding external batteries (but see [below](#danger-robot-stability)).

**Example 2**: The robot performs flawlessly in an air conditioned lab, but falls over frequently when deployed in a hot sunny environment. In this case, different joint are probably overheating, switching the system to emergency damp mode, resulting in a fall and damage to the robot. 

**Potential Solution**: ensure that your software is monitoring the temperature and currents of all joints. If your software detects operation near the thermal limits, warn bystanders and perform a safe sink-to-floor action with an audible alarm and flashing light alarm.   

<!-- TOC --><a name="danger-robot-stability"></a>
## DANGER: Robot Stability

**CAUTION: adding extra mass (such as external computers, sensors, grippers, and batteries) to the robot will affect your motion policies and the robot's stability and ability to navigate terrain. You may observe the robot swaying back and forth while simply trying to stand. Solution: train custom motion policies for your robot in its final mass configuration.**