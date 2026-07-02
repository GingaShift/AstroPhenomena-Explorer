# Design Overview — AstroPhenomena Explorer

AstroPhenomena Explorer is designed as a premium digital observatory interface.

The visual direction combines:

- scientific mission-control dashboard;
- astronomical atlas;
- interactive learning laboratory;
- observation planning interface;
- future research workspace.

The goal is not to create a generic space-themed website, but a serious and immersive scientific platform for understanding, visualizing and predicting astronomical phenomena.

---

## Visual Direction

The interface should feel:

- dark and premium;
- scientific and precise;
- calm, not gaming-like;
- object-centered when exploring celestial bodies;
- data-driven when planning observations;
- pedagogical when explaining phenomena.

Main visual language:

- deep black / dark navy background;
- thin technical grid;
- cyan active states;
- violet secondary accents;
- amber event highlights;
- modular scientific cards;
- central scientific canvas;
- side panels for metrics and explanations;
- progressive disclosure through Science Core drawers.

---

## Current Stitch Explorations

### Home / Overview

![Home Overview](assets/design/stitch_01_home_overview.png)

Introduces the project mission, the five scientific axes and the learning path:

Locate → Observe → Predict → Simulate → Analyze

---

### Sky Coordinates Explorer

<img width="2676" height="1873" alt="screen" src="https://github.com/user-attachments/assets/ca7ea4e3-4485-408d-98dd-75756e9d4886" />


First implementation target.

This screen answers:

> Where is this object in my sky right now?

It connects object coordinates, observer location and time to altitude, azimuth and visibility.

---

### Design System
<img width="1042" height="1600" alt="screen" src="https://github.com/user-attachments/assets/edeefcad-c4de-4a33-819e-496d70c55245" />


Defines the visual foundation:

- typography;
- colors;
- buttons;
- cards;
- badges;
- scientific visualization components.

---

### Cosmic Atlas — Moon Explorer

<img width="1600" height="1280" alt="screen" src="https://github.com/user-attachments/assets/774d71b8-16c3-4ac0-ad41-bdde6ff1b8f0" />


First object-centered immersive page.

The Moon becomes the emotional and scientific center of the interface, with live context, key facts, phase timeline and links to other tools.

---

### Observation Planner
<img width="1600" height="1280" alt="screen" src="https://github.com/user-attachments/assets/320fc9d9-6375-4e9b-aa9b-435927e1487f" />


Future observer-mode interface for planning a night of observation using altitude curves and visibility windows.

---

### Phenomena Detector

<img width="1600" height="1280" alt="screen" src="https://github.com/user-attachments/assets/d162ad79-5d2e-489c-811d-043db74fc849" />


Future prediction interface for astronomical configurations such as oppositions, conjunctions, transits and eclipses.

---

### Polaris Explorer

<img width="1600" height="1394" alt="screen" src="https://github.com/user-attachments/assets/f0a95a02-85b4-43e8-ac4b-5737484a54d2" />

Object-page concept explaining Polaris, the North Celestial Pole and the relationship between altitude and latitude.

---

### Research Workspace

<img width="1600" height="1280" alt="screen" src="https://github.com/user-attachments/assets/b645d373-ad53-4424-9d4b-6352c73d9a90" />


Future research-mode concept for analyzing curated astronomical datasets such as meteor shower observations.

---

### Simulation Lab

<img width="1920" height="1696" alt="screen" src="https://github.com/user-attachments/assets/8ea9ada5-215f-4517-99f7-5f3b5d2b87c1" />


Future simulation interface for explaining astronomical phenomena through geometric diagrams.

---

## Implementation Priority

The first coded prototype remains:

```txt
Sky Coordinates Explorer — Prototype 001
