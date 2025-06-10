# Augmented Reality Framework Overview

Augmented Reality on iOS is powered by **ARKit** and **RealityKit** — high-level frameworks offering robust APIs for world tracking, rendering, physics simulation, and shared experiences.  
**ARKit** focuses on scene understanding and motion tracking, while **RealityKit** provides a Swift-native Entity-Component System, photorealistic rendering, spatial audio, and animation support.

Together, they enable advanced features like:
- **LiDAR-based scene reconstruction**
- **Collaborative multi-device sessions**
- **Reality Composer integration for visual AR authoring**
- **SceneKit, SpriteKit, and Metal interoperability**

With these frameworks, you can easily add:

- **World Tracking** – 6DOF positional and rotational tracking using `ARSession` and `ARConfiguration`  
- **Plane Detection & Scene Understanding** – Automatic anchor detection (horizontal, vertical, image, object) with environment texturing  
- **Face & Body Tracking** – Real-time face mesh generation and full-body tracking with `ARBodyTrackingConfiguration`  
- **LiDAR & Depth API** – Access to `sceneDepth` and `confidenceMap` on supported devices for occlusion and mesh reconstruction  
- **Reality Composer Integration** – Design AR scenes visually and load `.reality` files with minimal code  
- **Entity-Component System (ECS)** – Modular control using `Entity`, `Component`, and `System` APIs in RealityKit  
- **Collaborative Sessions** – Share world maps and anchors between devices using RealityKit’s multiuser APIs  
- **Custom Rendering** – Combine ARKit with SceneKit, SpriteKit, or Metal for fine-tuned visuals and effects  

---

## Official Documentation

- [ARKit | Apple Developer Documentation](https://developer.apple.com/documentation/arkit)  
  Core APIs for motion tracking, hit testing, and scene understanding

- [RealityKit | Apple Developer Documentation](https://developer.apple.com/documentation/realitykit)  
  High-performance 3D simulation, rendering, and physics for AR experiences

- [Reality Composer | Apple Developer Documentation](https://developer.apple.com/documentation/realitycomposer)  
  Visual editor for building and previewing AR scenes

---

## Human Interface Guidelines

- [Augmented Reality HIG](https://developer.apple.com/design/human-interface-guidelines/augmented-reality/)  
  Guidelines for intuitive AR interactions and user comfort

- [Human Interface Guidelines Home](https://developer.apple.com/design/human-interface-guidelines/)  
  Best practices across all Apple platforms

---

## WWDC Videos

- [Introducing ARKit (WWDC 2017, Session 602)](https://developer.apple.com/videos/play/wwdc2017/602/)  
  ARKit fundamentals: world tracking, scene understanding, and integration with SceneKit & Metal

- [Explore ARKit 4 (WWDC 2020, Session 10611)](https://developer.apple.com/videos/play/wwdc2020/10611/)  
  LiDAR-driven depth API and raycasting improvements

- [Building AR Experiences with Reality Composer (WWDC 2019, Session 609)](https://developer.apple.com/videos/play/wwdc2019/609/)  
  Prototype AR scenes and import Reality files

- [Building Apps with RealityKit (WWDC 2019, Session 605)](https://developer.apple.com/videos/play/wwdc2019/605/)  
  RealityKit’s ECS for animation, physics, and networking

- [Dive into RealityKit 2 (WWDC 2021, Session 10074)](https://developer.apple.com/videos/play/wwdc2021/10074/)  
  RealityKit 2 enhancements: character controllers, face mesh, and more

- [Building Collaborative AR Experiences (WWDC 2019, Session 610)](https://developer.apple.com/videos/play/wwdc2019/610/)  
  Shared world maps and multi-device AR synchronization

---

## Example App

**Measure** – Apple’s built-in app using ARKit tracking, plane detection, and LiDAR to provide accurate real-world measurements.  

![Screenshot_2025-06-10_at_1 41 45_PM-removebg-preview](https://github.com/user-attachments/assets/4d5bd262-0281-433d-8a62-a2f8170db296)


**Download**: [Measure](https://apps.apple.com/sg/app/measure/id1383426740) – *Free*

---

## Summary

**ARKit** and **RealityKit** form a comprehensive AR platform on iOS — from low-level tracking and scene analysis to high-level visual composition and multiuser interactions.  
They abstract complex vision and rendering systems behind intuitive Swift APIs, empowering developers to build immersive, high-fidelity AR experiences across Apple devices.
