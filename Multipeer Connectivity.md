# Multipeer Connectivity Framework Overview

**Multipeer Connectivity** is Apple’s high-level peer-to-peer networking framework for discovering and communicating with nearby devices across **iOS**, **macOS**, and **tvOS**.  

It abstracts underlying transports like **Wi-Fi**, **peer-to-peer Wi-Fi**, **Bluetooth**, and **Ethernet**, enabling seamless, secure communication with a unified API.

At the core of the framework is `MCSession`, which manages peer connections via `MCPeerID`. Peer discovery is handled through the built-in `MCBrowserViewController` for plug-and-play UI or the lower-level `MCNearbyServiceBrowser` and `MCNearbyServiceAdvertiser` for fully customized discovery flows.

With Multipeer Connectivity, you can easily add:

- **Peer Discovery & Advertising** – Use `MCBrowserViewController` for automatic browsing or implement `MCNearbyServiceBrowser` and `MCNearbyServiceAdvertiser` for programmatic control  
- **Session Management** – Create `MCSession` instances to manage connections and monitor peer state changes via `session(_:peer:didChange:)`  
- **Data Messaging** – Send small data payloads reliably or unreliably with `send(_:toPeers:with:)`, handling errors with `MCError`  
- **Resource & File Transfer** – Send files using `sendResource(at:withName:toPeer:withCompletionHandler:)` and monitor progress through delegate callbacks  
- **Stream Connectivity** – Open `InputStream`/`OutputStream` with `startStream(withName:toPeer:)` for continuous, low-latency data flow  
- **Cross-Platform Support** – Available on iOS, macOS, and tvOS with automatic adaptation to available network interfaces  
- **Built-In UI** – Present `MCBrowserViewController` for quick peer discovery and session joining  
- **Security & Encryption** – All communication is encrypted via **DTLS**, with configurable modes: `MCEncryptionNone`, `MCEncryptionOptional`, or `MCEncryptionRequired`  
- **Customizable Discovery** – Filter and manage peer invitations using delegate methods for advanced workflows

---

## Official Documentation

- [Multipeer Connectivity | Apple Developer Documentation](https://developer.apple.com/documentation/multipeerconnectivity)  
  Reference for `MCSession`, `MCPeerID`, `MCBrowserViewController`, and more

---

## Human Interface Guidelines

- [Human Interface Guidelines Home](https://developer.apple.com/design/human-interface-guidelines/)  
  Best practices for designing intuitive peer connectivity flows

---

## Example Apps

**AirChat** – A free iOS app that can be used to message near by peers with Blutooth and other frameorks with no Data Usage

<img
  src="https://github.com/user-attachments/assets/8c5c2a26-5eb8-44fa-9594-3a2b704eacae"
  alt="…"
  style="width:300px; height:auto;"
/>

**Download**: [AirChat](https://apps.apple.com/sg/app/airchat-peer-to-peer-chat/id1606916296) – *Free*

---

## Summary

**Multipeer Connectivity** 
- provides a powerful, transport-agnostic framework for peer-to-peer communication, making it ideal for **multiplayer games**, **collaborative tools**, and **offline sharing apps**.  
- With support for secure messaging, file transfer, streaming, and discovery across Apple platforms, developers can build connected experiences with minimal setup and no server infrastructure.
