![Dog Backpack](https://github.com/user-attachments/assets/f3defe3e-7c6b-4db6-a260-7e872cf4ac9a)


# PRISM Backpack for Unitree Go2

## Introduction

The **PRISM Backpack** provides an easy to use, modular compute-and-development platform for robotics, seamlessly integrated with the Unitree Go2. 

Included is a full-suite of sensors that allow your Go2 to understand and react to its environment, and interact with people through OM1. The PRISM Backpack comes with OM1 fully built in - simply turn on the Go2 and OM1 will breathe life into your robot.

## Features

- **Powered by OM1** - Full suite of OM1 functionalities built-in.
- **Human in the Loop** - Connect and control your robot remotely, or request help from a professional whenever you need.
- **Developer Friendly** - Highly modular design with multiple connections and ports for easy hardware integration.

## Quick Start Guide


1. First, unplug the power and Ethernet cables that plug into the Unitree Go2 proprietary compute unit. 
2. Remove the compute unit:
    - Unscrew the 2 screws here (top), and here(back)
    - Remove the top lid, and unscrew the 4 screws attaching the lift handle.
    -  Reattach the lid, and screw in the top and back screws.
3. Attach the PRISM Base Mount Bracket to the bottom of the PRISM - Backpack. You may use adhesive.
4. After lining up the screw slots on the PRISM - Backpack:
    - Use the 25 mm Sockethead Screws to secure the top 2 slots.
    - Use the 30 mm Sockethead Screws to secure the bottom 2 slots.
5. Place the AGX Push Fit Bracket into the back of the Backpack Shell, taking care not to disrupt the cabling. 
6. Place the NVIDIA Jetson AGX on top of the bracket, aligning it with the raised pins on the bracket. Push from the top to secure it in place. 
7. Attach the Front Unit to the raised circular mount near the head of the Unitree Go2. You may use adhesive to secure it in place.
8. Connect the peripherals to the Jetson:
    - Waveshare USB Audio Driver
    - RJ45 Ethernet Cable from the Ethernet Hub
    - USB C to A Adapter - Intel 435i Depth Camera
    - USB B Data Cable - Front Unit USB Hub
    - HDMI to DP Adapter - HDMI cable for Front Screen
9. Connect the USB C to JST Connector to the Powerboard to power the Front Unit.
10. Connect the Split Power Cable to the Go2 Power Out, and the RJ45 to the Ethernet Board.
11. Plug in the 2.1 mm Power Barrel Jack from the Powerboard into the Jetson AGX.
12. Snap on the the lid, making sure that all cables are secured inside and none are left dangling.
13. Turn on the Unitree Go2.

## Documentation

- [Bill of Materials](./Docs/BoM.xlsx)
- [CAD Files](./CAD/)
- [Detailed Assembly Instructions and Custom Fabrication Guidelines](./Docs/Assembly.md)

## Repository Structure

```
PRISM/
├── README.md
├── docs/
│   ├── BoM.xlsx              # Bill of Materials
│   └── Assembly.md           # Assembly Instructions
├── cad/
    └── stl/                  # STL files for 3D printing
```

## License

This project is licensed under the terms of the **MIT License**, which is a permissive free software license that allows users to freely use, modify, and distribute the software. 

The MIT License is a widely used and well-established license that is known for its simplicity and flexibility. By using the MIT License, this project aims to encourage collaboration, modification, and distribution of the software.

---
