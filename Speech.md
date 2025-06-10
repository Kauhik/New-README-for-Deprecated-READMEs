# Speech Framework Overview

**Speech** is Apple’s high-level framework for performing both **live** and **file-based speech recognition** in iOS apps.  
It handles everything from user authorization and locale detection to task management and transcription metadata — providing a streamlined API that integrates seamlessly with **Swift** and **Xcode**.

With the Speech framework, you can easily add:

- **Authorization & Permissions** – Use `SFSpeechRecognizer.requestAuthorization(_:)` to prompt users and handle `SFSpeechRecognizerAuthorizationStatus` values like `.authorized` or `.denied`  
- **On-Device & Server-Based Recognition** – Choose between local recognition (privacy-first) or server-based recognition (better accuracy and language breadth)  
- **Live Audio Recognition** – Stream real-time audio via `SFSpeechAudioBufferRecognitionRequest` and receive live transcription updates  
- **File-Based Recognition** – Transcribe prerecorded files using `SFSpeechURLRecognitionRequest` to return a `SFSpeechRecognitionTask`  
- **Locale & Language Support** – Set custom locales using `Locale(identifier:)` and query supported options with `SFSpeechRecognizer.supportedLocales()`  
- **Task Management** – Monitor task progress with `SFSpeechRecognitionTask`, check `isFinal`, and handle task cancellation or failure via `SFSpeechRecognitionErrorCode`  
- **Alternative Transcriptions & Metadata** – Access transcription segments with `SFTranscription` for timestamps, confidence scores, and alternative phrasing  
- **Error Handling** – Gracefully handle permission errors, network issues, or service interruptions through task error inspection  
- **Sample Code & Tutorials** – Follow Apple's guides for live and file-based recognition implementations in Swift

---

## Official Documentation

- [Speech API Reference](https://developer.apple.com/documentation/speech)  
- [Recognizing Speech in Live Audio (Sample)](https://developer.apple.com/documentation/speech/recognizing-speech-in-live-audio)  
- [Transcribing Speech to Text (Tutorial)](https://developer.apple.com/tutorials/app-dev-training/transcribing-speech-to-text)  
- [Asking Permission to Use Speech Recognition](https://developer.apple.com/documentation/speech/asking-permission-to-use-speech-recognition)  
- [SFSpeechURLRecognitionRequest](https://developer.apple.com/documentation/speech/sfspeechurlrecognitionrequest)  
- [SFSpeechRecognizer](https://developer.apple.com/documentation/speech/sfspeechrecognizer)

---

## Human Interface Guidelines

- [Siri Voice Interactions](https://developer.apple.com/design/human-interface-guidelines/siri/)  

---

## WWDC Videos

- [Speech Recognition API (WWDC 2016)](https://developer.apple.com/videos/play/wwdc2016/509/)  
- [Advances in Speech Recognition (WWDC 2019)](https://developer.apple.com/videos/play/wwdc2019/256/)  
- [Customize On-Device Speech Recognition (WWDC 2023)](https://developer.apple.com/videos/play/wwdc2023/10101/)

---

## Example App

**Noted** – A one-tap recording app that uses the Speech framework to transcribe audio, recognize punctuation, and sync transcriptions via iCloud.  

<img
  src="https://github.com/user-attachments/assets/19b0c33a-9643-45ab-aae1-e498ce3acdfc"
  alt="image"
  width="300"
/>

**Download**: [Noted](https://apps.apple.com/sg/app/noted-record-ai-transcribe/id1149425482) – *Free*

---

## Summary

- The **Speech** framework enables developers to build intelligent voice-driven apps with minimal effort.  

- From microphone input and file-based transcription to real-time updates, alternative phrasing, and metadata access, its Swift-friendly API empowers seamless integration of **speech-to-text** functionality in modern iOS apps.
