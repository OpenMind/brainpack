
<img src="./docs/images/social_intelligence.png" alt="OpenMind Scoial Intelligence" width="800">

# BrainPack for Unitree G1, Unitree Go2, and LimX Tron 1

## Introduction

The **BrainPack** provides an easy to use, modular compute-and-development platform for robotics, seamlessly integrated with the Unitree G1, Unitree Go2, and LimX Tron 1 (and many other movement platforms, coming soon). 

Included is a full-suite of sensors that allow your robot to understand and react to its environment, and interact with humans. The BrainPack with [Nvidia Thor](https://developer.nvidia.com/blog/introducing-nvidia-jetson-thor-the-ultimate-platform-for-physical-ai/) can connect to OpenMind cloud endpoints for voice, spatial navigation, emotion generation, teleops, and other robot functionality. 

The overall purpose of the BrainPack is to empower rapid iteration. It enables developers and organizations to explore vertical-specific solutions quickly, reconfiguring the system efficiently to meet evolving customer needs without requiring extensive custom hardware builds.

## Cross-Platform - It's Wooftacular!

<img src="./docs/images/brainpack_go2.png" alt="BrainPack OverView" width="500">

## The Challenges in Robotics Development and Deployment

Currently, many robotics platforms are limited to pure academic research, single industrial problems, or for use as toys. When organizations attempt to deploy these robots into more complex and more realistic environments, significant limitations quickly become apparent.

### Hardware Limitations 

Common pain points include inadequate human-robot interfaces  (e.g. very weak or unadjustable speakers, lack of touchscreens, unsuitable microphones) and outdated or poorly documented secondary computing modules. For researchers and companies, this means that even when purchasing a powerful mobility platform, such as Unitree G1, substantial time and efforts must be spent building custom hardware including specialized cabling, 3D-printed parts, and add-on sensors, simply to conduct basic experiments and product development.

### Fragmentation and Scalability

The robotics landscape is massive and highly fragmented. With over 400 active companies developing diverse robotic platforms and form factors, one impediment is the lack of global standards. Currently, there are no standards for integrating or swapping key components — whether that involves sensors, computing power, or power dostribution.

This forces developers into a prohibitive cycle: when a product is built, it cannot be easily deployed across dozens, or even hundreds, of different robot brands and physical forms. This inefficiency means development efforts are tied to single-brand and single form factor platforms.

Developers should ideally be able to focus solely on creating advanced "robot skills" (intelligence), confident that those capabilities can be deployed across brands and form factors. The BrainPack solves this foundational problem. It provides a standardized interface, establishing a universal layer of capability that allows our software and intelligence to run across diverse robotic hardware platforms.

### Data Security and Privacy

Many users and customers expect full transparency and auditability of data collection and use, especially for highly sensitive data such as robot location, audio, video, and LiDAR. If all data are physically routed directly to a secondary compute module such as the excellent Nvidia Thor, then it is possible to audit and secure data collection and later processing/use. Similar considerations apply to all WiFi or Bluetooth transmissions between a robot and the internet. 

### Our Solution: The Brain Pack

We developed the BrainPack to address these systemic roadblocks. This modular system provides deployment flexibility by providing a streamlined architecture that makes it easy to integrate, adapt, and explore diverse use cases. Crucially, the BrainPack allows users to seamlessly add or subtract specific sensors, and even incorporate hardware-level Privacy Switches. These switches grant manual positive control, allowing users to enable or disable specific functions (like video streaming or audio capture) based on project requirements.

## Features

- **Powered by OM1** - Full suite of OM1 functionality built-in.
- **Human in the Loop** - Teleops - control your robot remotely or request help from another human whenever you need (via portal.openmind.com).
- **Developer Friendly** - Modular design with multiple connections and ports for easy hardware integration.

## Documentation

- [Bill of Materials](./docs/Materials.md)
- [CAD Files](./CAD/)
- [Assembly Instructions](./docs/Assembly.md)

## Repository Structure

```
PRISM/
├── README.md
├── docs/
│   ├── Materials.md       # Bill of Materials
│   └── Assembly.md        # Assembly Instructions
├── CAD/
    └──                    # STL files for 3D printing
```

## License

This project is licensed under the terms of the **MIT License**, which is a permissive free software license that allows users to freely use, modify, and distribute the software. 

The MIT License is a widely used and well-established license that is known for its simplicity and flexibility. By using the MIT License, this project aims to encourage collaboration, modification, and distribution of the software.

---
