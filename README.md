# TheraBeat
*This project was developed in my Applied Projects Capstone in Spring 2026*

TheraBeat is a browser-based interactive music web app that transforms hand gestures into sound using computer vision and audio. 
TheraBeat introduces the idea of the **TheraZone** — a gesture-controlled interaction space that turns movement into music.

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
## Idea of TheraZone

**TheraZone** is the interactive camera-based input area where gestures are detected and translated into sound.

### Features

#### Visual Metronome

A visual beat indicator helps users stay in rhythm.

#### Hand-Only Detection
 
Only hand movements inside the designated TheraZone are processed.
  - Movements outside the zone are ignored.
  - Non-hand objects (e.g., pets, background motion) are ignored.
  - Left and right hands are distinguished.

#### Object Segmentation & Calibration

OpenCV-based segmentation helps isolate hands during setup and improve detection accuracy.

---
## Camera-Based Instruments

TheraBeat translates hand tracking movements into playable instruments:

### Theremin
- Inspired by the original theremin.
- Hand position controls pitch and frequency using camera tracking instead of electromagnetic fields.
### Drums
- Finger-to-thumb contact triggers drum components.
- Different gestures map to different drum pieces.
  
### Future Iterated Instrument Ideas 
These instruments weren't developed for use in the **TheraZone** due to time on the project and lack of research for these instruments being detecting via Computer Vision for the time being (Piano, Guitar). 

### Custom Gestures
Users can:
- Create custom gesture mappings
- Modify transitions between instruments
- Save specific gestures per project

## Tech Stack Used 
This project utilizes Next.js, Tone.js, MediaPipe, and OpenCV. 
