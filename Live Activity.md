# Live Activities Framework Overview

**Live Activities** is Apple’s high-level mechanism for delivering real-time updates directly to the **Lock Screen**, **Dynamic Island**, **StandBy**, **CarPlay**, and **Apple Watch Smart Stack**.  

Built on the **ActivityKit** framework, it provides APIs to request, update, and end Live Activities both locally and via push notifications — keeping users engaged without re-entering the app.

With Live Activities, you can easily add:

- **ActivityKit APIs** – Use `Activity.request(attributes:content:pushType:)` to create a Live Activity, `activity.update(...)` to refresh it, and `activity.end(...)` to close it with final state  
- **Attributes & Content State** – Define a `struct` conforming to `ActivityAttributes`, including a nested `ContentState` for dynamic properties in a type-safe, `Codable` way  
- **Lock Screen Presentation** – Implement `ActivityConfiguration` in SwiftUI for glanceable, styled views on the Lock Screen  
- **Dynamic Island Support** – Supply views for `compactLeading`, `compactTrailing`, `minimal`, and `expanded` modes for rich presence on iPhone 14 Pro and later  
- **StandBy & CarPlay Integration** – Live Activities automatically appear in StandBy mode and in CarPlay, adapting layouts for readability  
- **Push-Driven Updates** – Enable remote updates using the `liveactivity` pushType; ActivityKit handles delivery constraints and fallbacks  
- **WidgetKit Interactivity** – Starting in iOS 17, embed tappable buttons and toggles with WidgetKit SwiftUI APIs for in-place actions  
- **Multi-Device Sync** – Automatically mirror Live Activities to Apple Watch Smart Stack and compatible Mac layouts  
- **Lifecycle & State Handling** – Track state changes via `activity.activityStateUpdates` (`.started`, `.dismissed`, `.stale`, etc.), and control dismissal timing

---

## Official Documentation

- [ActivityKit | Apple Developer Documentation](https://developer.apple.com/documentation/activitykit)  
  Core APIs for managing Live Activities across platforms

- [Displaying live data with Live Activities](https://developer.apple.com/documentation/activitykit/displaying-live-data-with-live-activities)  
  SwiftUI layout and update guidance

- [Push updates for Live Activities](https://developer.apple.com/documentation/activitykit/starting-and-updating-live-activities-with-activitykit-push-notifications)  
  How to configure pushType and manage push tokens

---

## Human Interface Guidelines

- [Live Activities HIG](https://developer.apple.com/design/human-interface-guidelines/live-activities)  
  Best practices for designing glanceable, real-time interfaces

---

## WWDC Videos

- [Meet ActivityKit (WWDC 2023, Session 10184)](https://developer.apple.com/videos/play/wwdc2023/10184/)  
  Lifecycle, SwiftUI layout composition, and update techniques

- [Design Dynamic Live Activities (WWDC 2023, Session 10194)](https://developer.apple.com/videos/play/wwdc2023/10194/)  
  Layout creation and performance considerations

- [Bring Live Activity to Apple Watch (WWDC 2024, Session 10068)](https://developer.apple.com/videos/play/wwdc2024/10068/)  
  Smart Stack integration and update reliability

- [Interactivity in Widgets and Live Activities (WWDC 2022)](https://developer.apple.com/videos/play/wwdc2022/10054/)  
  How to add buttons, toggles, and real-time responses

---

## Example App

**CARROT Weather** – Get up-to-the-minute forecasts on your Lock Screen via a Live Activity.Transient and continuous haptic cues can even accompany sudden weather alerts. 

<img
  src="https://github.com/user-attachments/assets/e075d9fb-2bd6-4109-8912-252ae6ffb2b7"
  alt="…"
  width="300"
/>

**Download**: [CARROT Weather](https://apps.apple.com/sg/app/carrot-weather-alerts-radar/id961390574) – *Free*

---

## Summary

Live Activities, powered by **ActivityKit** and **WidgetKit**, enable real-time, glanceable, and interactive experiences across iPhone, iPad, Apple Watch, and CarPlay.  
By combining type-safe attributes, SwiftUI-powered layouts, push-based updates, and state lifecycle APIs, developers can deliver engaging content that stays seamlessly synchronized across platforms — without interrupting user flow.
