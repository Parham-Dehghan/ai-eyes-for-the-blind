# 🧠 AI Accessibility Suite – PolyVoice, Real-Time Communication, and md

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg) ![Status: Active](https://img.shields.io/badge/Status-Active-green.svg)

This repository provides three AI-powered applications designed to empower individuals with **speech**, **hearing**, and **vision** impairments. Built with accessibility, inclusiveness, and real-world usability in mind, these tools aim to bridge communication gaps and enhance independence.

---

## 🗣️ PolyVoice: Text-to-Speech for Non-Verbal and Mute Users

**PolyVoice** is a user-friendly text-to-speech application tailored for individuals unable to speak due to physical or medical conditions, enabling real-time conversion of typed text into natural-sounding speech.

### 🔧 Key Features
| Feature | Description |
|---------|-------------|
| **Text-to-Speech Conversion** | Converts typed text into natural audio using AI-based engines (e.g., gTTS, Tortoise). |
| **Multilingual Support** | Supports multiple languages and accents for global accessibility. |
| **Custom Voice Settings** | Allows selection of male/female tones, pitch, and speed adjustments. |
| **Offline Mode** | Optional functionality for use without internet connectivity. |
| **Emotion Synthesis** | Optional feature to add emotional tones (e.g., happy, sad) to speech. |

### 🧑‍🤝‍🧑 Target Audience
- Individuals with speech impairments (e.g., ALS, stroke, autism).
- Therapists and caregivers facilitating communication.
- Users experiencing temporary voice loss.

### 🧠 System Workflow
```mermaid
flowchart TD
    Input[User Types Message] --> Config[Configure Voice Settings<br>(Language, Pitch, Speed)]
    Config --> Process[Preprocess Text]
    Process --> Engine[Select TTS Engine<br>(e.g., gTTS, Tortoise)]
    Engine --> Output[Audio Playback]
    Output -->|Adjust Settings| Config
```

**Flowchart Description**: The PolyVoice flowchart is a linear diagram with a feedback loop, rendered as a top-down sequence of rectangular nodes connected by arrows. It starts with a node labeled "User Types Message," flowing to "Configure Voice Settings (Language, Pitch, Speed)," then to "Preprocess Text," followed by "Select TTS Engine (e.g., gTTS, Tortoise)," and finally to "Audio Playback." A dashed arrow labeled "Adjust Settings" loops back from "Audio Playback" to "Configure Voice Settings," indicating the user can refine settings after playback. The nodes are styled with rounded corners and a light background, typical of Mermaid’s default rendering on GitHub.

### 💻 How to Run
```bash
pip install -r requirements.txt
python polyvoice_main.py
```

---

## 🔁 Real-Time Communication: Speech ↔ Text Interface

**Real-Time Communication** enables seamless interaction between deaf or mute individuals and hearing people by converting speech to text and typed text to speech in real time.

### 🔧 Key Features
| Feature | Description |
|---------|-------------|
| **Speech Recognition (ASR)** | Instantly converts speech to text using Whisper or other ASR models. |
| **Text-to-Speech Output** | Converts typed responses into spoken language. |
| **Custom Interfaces** | Adjustable font size, color themes, and layouts for enhanced visibility. |
| **Microphone & Speaker Integration** | Optimized for real-time conversational use. |

### 🧑‍🤝‍🧑 Target Audience
- Deaf, hard-of-hearing, or mute individuals.
- Public service desks (e.g., banks, clinics) for inclusive communication.
- Educators and interpreters.

### 🧠 System Workflow
```mermaid
flowchart TD
    Start[Start Conversation] --> Config[Customize Interface<br>(Font, Colors, Layout)]
    Config --> Mic[Microphone Input]
    Mic --> ASR[ASR Engine<br>(Speech-to-Text)]
    ASR --> Display[Display Text on Screen]
    Display --> Type[User Types Response]
    Type --> TTS[TTS Engine<br>(Text-to-Speech)]
    TTS --> Speaker[Speaker Output]
    Speaker -->|Continue Conversation| Mic
```

**Flowchart Description**: The Real-Time Communication flowchart is a cyclical diagram, rendered top-down with rectangular nodes and arrows. It begins with "Start Conversation," leading to "Customize Interface (Font, Colors, Layout)," then to "Microphone Input," followed by "ASR Engine (Speech-to-Text)," "Display Text on Screen," "User Types Response," "TTS Engine (Text-to-Speech)," and "Speaker Output." A dashed arrow labeled "Continue Conversation" loops back from "Speaker Output" to "Microphone Input," representing the ongoing conversational cycle. The nodes have rounded corners, with text centered and arrows clearly indicating flow direction.

### 💻 How to Run
```bash
pip install -r requirements.txt
python real_time_main.py
```

---

## 🤖 md: AI Assistant for the Blind and Deaf

**md** (Multi-Disability Assistant) is an intelligent assistant for **blind and deaf users**, using real-time camera input, object detection, OCR, and AI to describe environments via audio or text.

### 🔧 Key Features
| Feature | Description |
|---------|-------------|
| **Dual Mode (Blind/Deaf)** | Selectable mode for blind or deaf users on startup. |
| **Object Detection** | Identifies people, objects, and obstacles using YOLO/SSD models. |
| **Text Recognition (OCR)** | Reads signs, books, and handwritten or printed content. |
| **Scene Description** | Generates detailed descriptions of complex scenes. |
| **Multi-Output Interface** | Audio narration (TTS) for blind users; text and vibration alerts for deaf users. |

### 🧑‍🤝‍🧑 Target Audience
- Blind or low-vision users needing contextual feedback.
- Deaf users requiring visual alerts or text summaries.
- Public assistive installations and wearable devices.

### 🧠 System Workflow
```mermaid
flowchart TD
    Start[Launch App] --> Mode{Select Mode: Blind or Deaf}
    Mode -->|Blind| Cam[Capture via Camera]
    Mode -->|Deaf| Cam
    Cam --> Vision[AI Analysis<br>(Object Detection, OCR, Scene Description)]
    Vision -->|Blind| Audio[TTS Voice Output]
    Vision -->|Deaf| Output[Text Summary + Visual UI<br>+ Optional Vibration Alerts]
    Output -->|User Feedback| Cam
    Audio -->|User Feedback| Cam
```

**Flowchart Description**: The md flowchart is a branching diagram, rendered top-down with a decision node and parallel paths. It starts with "Launch App," leading to a diamond-shaped decision node "Select Mode: Blind or Deaf." Two arrows branch out: one labeled "Blind" and one labeled "Deaf," both pointing to a shared "Capture via Camera" node. This flows to "AI Analysis (Object Detection, OCR, Scene Description)." From there, two paths diverge: the "Blind" path leads to "TTS Voice Output," and the "Deaf" path leads to "Text Summary + Visual UI + Optional Vibration Alerts." Dashed arrows labeled "User Feedback" loop back from both output nodes to "Capture via Camera," indicating continuous interaction. Nodes are styled with rounded corners (rectangular) or diamonds (decision), with clear labels and arrows.

### 💻 How to Run
```bash
pip install -r requirements.txt
python md.py
```

---

## 📁 Project Structure

```
ai-accessibility-suite/
│
├── polyvoice_main.py         # PolyVoice app
├── real_time_main.py         # Real-Time Communication tool
├── md.py                     # md assistant
├── requirements.txt
├── README.md
└── assets/
    └── screenshots/
```

---

## 🔐 Accessibility Principles

- **WCAG Compliance**: High-contrast design with readable fonts.
- **Voice-Free Interaction**: Fully usable without audio in Deaf Mode.
- **Large Buttons & Simple UI**: Suitable for low-vision or elderly users.
- **Keyboard Accessibility**: All features navigable without a mouse.

---

## 📜 License

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg)

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**. You are free to share and adapt the material for non-commercial purposes with proper attribution.

🔗 [License Details](https://creativecommons.org/licenses/by-nc/4.0/)

---

## 💡 Future Features (Planned)

- [ ] Sign language recognition and feedback
- [ ] Braille printer integration
- [ ] Mobile app versions for Android/iOS
- [ ] Cloud data sharing for caregivers

---

## 🙌 Contribution

We welcome contributions from developers, designers, accessibility researchers, and community members. Please submit issues or pull requests on [GitHub](https://github.com/Parham-Dehghan).

> **Designed to empower communication for all – regardless of ability.** 🌍

---

## 👨‍💻 Creator Information

| Name | Mohammad Parham Dehghan |
|------|-------------------------|
| **Email** | dehghanparham6@gmail.com |
| **YouTube** | [AI Accessibility Projects & Demos](https://youtube.com) |
| **GitHub** | [@Parham-Dehghan](https://github.com/Parham-Dehghan) |

---

## 📜 License (Repeated for Clarity)

![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg)

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)**. For more details, visit [creativecommons.org/licenses/by-nc/4.0](https://creativecommons.org/licenses/by-nc/4.0/).
