# TheraBeat

TheraBeat is a browser-based interactive music creation platform that transforms hand gestures into sound using real-time computer vision and audio synthesis.

Built for users familiar with music software, TheraBeat introduces **TheraZone** — a gesture-controlled interaction space that turns movement into music.

---

## Overview

TheraBeat allows users to:

- Create new music projects
- Add and manage tracks
- Record using gesture-based instruments
- Customize gestures
- Save and export compositions

The system combines real-time hand tracking, object segmentation, and web-based audio synthesis to provide a seamless creative workflow.

---

## Core Concept: TheraZone

**TheraZone** is the interactive camera-based input area where gestures are detected and translated into sound.

### Features

- **Visual Metronome**  
  A visual beat indicator helps users stay in rhythm.

- **Hand-Only Detection**  
  Only hand movements inside the designated TheraZone are processed.
  - Movements outside the zone are ignored.
  - Non-hand objects (e.g., pets, background motion) are ignored.
  - Left and right hands are distinguished.

- **Object Segmentation & Calibration**  
  OpenCV-based segmentation helps isolate hands during setup and improve detection accuracy.

---

## 🎹 Camera-Based Instruments

TheraBeat translates gestures into playable instruments:

### 🎼 Piano
- Hand movements map to piano keys.
- Optional “table mode” allows playing on a flat surface.

### 🥁 Drums
- Finger-to-thumb contact triggers drum components.
- Different gestures map to different drum pieces.

### 🎸 Guitar
- Air guitar strumming translates into actual guitar sounds.

### 🎛 Theremin
- Inspired by the original theremin.
- Hand position controls pitch and frequency using camera tracking instead of electromagnetic fields.

### ✨ Custom Gestures
Users can:
- Create custom gesture mappings
- Modify transitions between instruments
- Save specific gestures per project

---

## 🎓 Tutorial

The tutorial assumes prior experience with music software.

It focuses on:
- Using TheraZone
- Calibrating hand detection
- Mapping gestures to instruments
- Recording and playback workflow

---

## 💾 Saving & Exporting

Users can:

- Save projects (gesture mappings, track data, metadata)
- Export music files (MP3, WAV, MP4)
- Store recordings in cloud storage

On first use, users are prompted with:

> "Would you like to enable cloud saving and export functionality?"

---

## 🏗 Tech Stack

### 🖥 Frontend
- **Next.js**  
  Handles UI components, routing, structure, and overall application interface.  
  https://nextjs.org/

### 🔊 Audio Engine
- **Tone.js**  
  Web Audio framework powering:
  - Synths
  - Instrument playback
  - Sequencing
  - Real-time interaction  
  https://tonejs.github.io/

### 👁 Computer Vision

- **MediaPipe Holistic Landmarker**  
  Provides:
  - Real-time hand landmark detection
  - Gesture tracking
  - Vision-to-audio mapping  
  https://ai.google.dev/edge/mediapipe/solutions/vision/holistic_landmarker

- **OpenCV**  
  Used for:
  - Object segmentation
  - Calibration steps
  - Hand isolation
  - Left/right hand differentiation  

### ☁ Storage

- Cloud-based storage (planned)
- Research target: Amazon S3 Object Storage
  - Store MP3, WAV, MP4 files
  - Save metadata (URL paths, project data)

---

## 🧩 Functional Prototype Structure

### Frontend (Next.js)
- Project creation UI
- Track management
- Instrument selection
- Gesture customization panel
- Recording controls
- Export interface

### Audio Layer (Tone.js)
- Synth and instrument routing
- Beat synchronization
- Visual metronome sync
- Recording buffer management

### Vision Layer (MediaPipe + OpenCV)
- Camera input
- Landmark detection
- TheraZone filtering
- Gesture classification
- Segmentation-based calibration

### Storage Layer
- Project metadata persistence
- Cloud-based object storage integration

---

## 🛠 Development Setup

```bash
# Install dependencies
npm install

# Run development server
npm run dev
