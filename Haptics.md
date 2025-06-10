# Core Haptics Framework Overview

**Core Haptics** is Apple’s high-level framework for designing and playing customized haptic patterns synchronized with audio.  
It abstracts the Taptic Engine and Core Audio layers behind a unified API, enabling developers to create immersive, low-latency tactile experiences.

The framework revolves around `CHHapticEngine`, which manages communication with the haptic hardware and audio session, and uses `CHHapticPattern`, `CHHapticEvent`, and `CHHapticParameterCurve` objects to build rich feedback patterns.  
Real-time playback and parameter modulation are supported via `CHHapticPatternPlayer` and `CHHapticAdvancedPatternPlayer`.

With Core Haptics, you can easily add:

- **Haptic Engine** – Instantiate `CHHapticEngine` to start a session, handle engine resets, and manage playback lifecycle  
- **Pattern Events** – Define transient and continuous events with `CHHapticEvent`, specifying intensity, sharpness, and timing  
- **Parameter Curves** – Use `CHHapticParameterCurve` for gradual property changes like frequency or intensity over time  
- **Audio Integration** – Sync sound and vibration by registering audio resources via `CHHapticAudioResourceID`  
- **Real-Time Control** – Use pattern players to pause, stop, resume, and dynamically adjust playback on-the-fly  
- **Apple Haptic Audio Pattern (AHAP)** – Store haptic patterns in JSON-based `.ahap` files for easy sharing and updates  

---

## Official Documentation

- [Core Haptics | Apple Developer Documentation](https://developer.apple.com/documentation/corehaptics)  
  Overview of classes like `CHHapticEngine`, `CHHapticPattern`, and pattern players for custom feedback

- [Preparing Your App to Play Haptics](https://developer.apple.com/documentation/corehaptics/preparing_your_app_to_play_haptics)  
  Learn how to check device compatibility, configure the engine, and register haptic/audio resources

---

## WWDC Videos

- [Introducing Core Haptics (WWDC 2019, Session 520)](https://developer.apple.com/videos/play/wwdc2019/520/)  
  Core APIs overview, pattern construction, and playback best practices

- [Expanding the Sensory Experience with Core Haptics (WWDC 2019, Session 223)](https://developer.apple.com/videos/play/wwdc2019/223/)  
  Principles for combining haptics, sound, and visuals for immersive design

- [Practice Audio Haptic Design (WWDC 2021, Session 10278)](https://developer.apple.com/videos/play/wwdc2021/10278/)  
  Sample project: **HapticBounce** – demonstrating real-time parameter control and audio sync

- [Advancements in Game Controllers (WWDC 2020, Session 10614)](https://developer.apple.com/videos/play/wwdc2020/10614/)  
  Using Core Haptics with Game Controller framework for custom game rumble

---

## Example App

**Haptrix** – Browse and load custom haptic-and-audio patterns (AHAP files) from the web or your device and can pair with its macOS companion to design haptics on desktop and instantly feel them on your iPhone

<img src="https://github.com/user-attachments/assets/0abed5df-b93a-401a-84af-3c64a404e5cd" alt="…" width="300"/>

**Download**: [Haptrix](https://apps.apple.com/sg/app/haptrix/id1467942077) – *Free*

---

## Summary

Core Haptics empowers developers to go beyond standard feedback generators with a powerful, event-based system for designing precise and immersive haptic-audio interactions.  
With support for engine sessions, dynamic playback, audio sync, and AHAP files, it unlocks expressive tactile design across iPhone, iPad, and Apple Watch (Series 4+) devices.
