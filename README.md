# naruto-hand-tracking-.
Interactive webcam-based Naruto and Sasuke power effects powered by MediaPipe Hands.

# 🌀 Naruto & Sasuke Hand Tracking Effects (MediaPipe Project)

A real-time **web-based hand tracking system** that uses MediaPipe Hands to detect user gestures through a webcam and triggers Naruto and Sasuke animated effects based on hand movement.

The system overlays anime-style visuals on top of live camera input and reacts dynamically to finger gestures.

---

## 🎯 Project Overview

This project uses **computer vision (MediaPipe Hands)** to track 21 hand landmarks in real time. It detects whether a hand is open or closed by analyzing finger positions relative to the wrist.

When a hand is detected as **open**, an anime power effect is triggered:
- Left hand → Naruto effect
- Right hand → Sasuke effect

The effect follows the hand position on screen and fades smoothly based on gesture activity.

---

## ⚙️ How It Works (Core Logic)

### 1. Hand Detection
- MediaPipe detects up to **2 hands simultaneously**
- Each hand provides **21 landmark points**

### 2. Gesture Recognition
The function:

```javascript
checkOpen(pts)
