# SharePlay Framework Overview

**SharePlay** is Apple’s high-level framework for enabling synchronized media and interactive experiences across multiple users through **FaceTime**, **Messages**, and system-level collaboration interfaces.  
Powered by the **Group Activities** and **Group Session** APIs, it abstracts session management, state sync, and UI integration — enabling seamless real-time collaboration.

With SharePlay, you can easily add:

- **GroupActivity Definition** – Define a `struct` conforming to `GroupActivity` to represent your shared experience and activity logic  
- **GroupSession Management** – Use `GroupSession<MyActivity>` to join, start, or leave a session; monitor session lifecycle with `GroupSessionWatcher`  
- **State Synchronization** – Expose dynamic, `Codable` content via `ContentState` for automatic real-time sync across participants  
- **Real-Time Messaging** – Send and receive custom payloads with `GroupSessionMessenger` to power collaborative features  
- **Media Playback Sync** – Coordinate `AVPlayer` and system media controls for frame-accurate playback sync across all users  
- **System UI Integration** – Use `UIActivityViewController`, SharePlay buttons, and overlays to initiate sessions with minimal code  
- **Multi-Platform Support** – Works across iOS, iPadOS, macOS, tvOS, and visionOS with consistent APIs  
- **Security & Privacy** – Built-in user consent via FaceTime, end-to-end encryption, and privacy-first architecture

---

## Official Documentation

- [Group Activities | Apple Developer Documentation](https://developer.apple.com/documentation/groupactivities)  
  Overview of APIs for enabling and managing SharePlay sessions

---

## Human Interface Guidelines

- [SharePlay HIG](https://developer.apple.com/design/human-interface-guidelines/shareplay)  
  Best practices for shared experiences, invitations, and session feedback

---

## WWDC Videos

- [Meet Group Activities (WWDC 2021, Session 10183)](https://developer.apple.com/videos/play/wwdc2021/10183/)  
  High-level introduction to SharePlay’s architecture and media syncing

- [What’s New in SharePlay (WWDC 2022, Session 10140)](https://developer.apple.com/videos/play/wwdc2022/10140/)  
  Recent API enhancements and design strategies

- [Add SharePlay to Your App (WWDC 2023, Session 10239)](https://developer.apple.com/videos/play/wwdc2023/10239/)  
  Hands-on demo: building shared experiences with the latest features

---

## Example App

**DrawTogether** – A collaborative whiteboard app shown at WWDC 2023 using `GroupSessionJournal` for real-time drawing sync across multiple users via SharePlay.

<img
  src="https://github.com/user-attachments/assets/b1c6d059-0a7a-467b-93f3-65da718b8bbf"
  alt="…"
  width="300"
/>

**Download**: [DrawTogether](https://apps.apple.com/sg/app/drawtogether-enjoy-drawing/id1445350507) – *Free*

---

## Summary

**SharePlay**, built on the **Group Activities** framework, simplifies synchronized interaction and playback experiences across Apple platforms.  
With declarative activity definitions, secure session handling, and deep system integration, developers can create engaging, real-time features — from collaborative tools to media sharing — without dealing with low-level networking or state management complexities.
