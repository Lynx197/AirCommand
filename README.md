# AI Gesture Controller ✋🖱️

[](https://www.python.org/downloads/)
[](https://developers.google.com/mediapipe)
[](https://opencv.org/)

A touchless interface for Windows that uses real-time hand gestures to control the mouse, scrolling, system volume, and screen brightness. Built with Python, OpenCV, and Google's MediaPipe.

> **Note:** This project requires a webcam.

## ✨ Features

  * **Mouse Control:** Move the cursor with natural hand movements.
  * **Clicking:** Left click, right click, and double click using finger gestures.
  * **Drag & Drop:** Grip your hand into a fist to click and drag items.
  * **Scrolling:** Vertical and horizontal scrolling using your non-dominant hand.
  * **System Controls:** Adjust volume and brightness with simple pinch gestures.
  * **Smooth Tracking:** Implements dampening for stable cursor movement.

## 🛠️ Prerequisites

Due to current library limitations (specifically MediaPipe), this project **does not support Python 3.13**.

  * **Python:** Version 3.10, 3.11, or 3.12 is required.
  * **OS:** Windows 10/11 (required for Pycaw volume control and brightness control).
  * **Webcam:** Any standard USB or integrated webcam.

## 📦 Installation

1.  **Clone the repository**

    ```bash
    git clone https://github.com/YOUR_USERNAME/REPO_NAME.git
    cd REPO_NAME
    ```

2.  **Create and activate a virtual environment (Recommended)**

    ```bash
    # For Windows
    py -3.12 -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install dependencies**

    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Usage

1.  Run the script:

    ```bash
    python gesture_controller.py
    ```

    *(Note: You may need to run your terminal as Administrator for volume/brightness controls to work properly depending on your system security settings.)*

2.  The application window will open, showing your webcam feed with hand landmarks.

## 📖 Gesture Guide

The system automatically detects your dominant (Right) and non-dominant (Left) hands.

### 🖱️ Mouse Controls (Dominant Hand - Default: Right)

| Action | Gesture | Description |
| :--- | :--- | :--- |
| **Move Cursor** | ✌️ **V-Sign** | Index and Middle fingers UP. |
| **Left Click** | 🖕 **Middle Finger Up** | From V-Sign, quickly lower your index finger. |
| **Right Click** | ☝️ **Index Finger Up** | From V-Sign, quickly lower your middle finger. |
| **Double Click** | ✌️ **Two Fingers Closed** | From V-Sign, bring index and middle fingers together. |
| **Drag & Drop** | ✊ **Fist** | Close entire hand while hovering over an item. |

### 🎛️ System Controls (Dominant Hand - Default: Right)

| Action | Gesture | Description |
| :--- | :--- | :--- |
| **Volume Control** | 👌 **Pinch & Move Vertically** | Pinch Index & Thumb. Move hand UP to increase volume, DOWN to decrease. |
| **Brightness** | 👌 **Pinch & Move Horizontally** | Pinch Index & Thumb. Move hand RIGHT to increase brightness, LEFT to decrease. |

### 📜 Scrolling (Non-Dominant Hand - Default: Left)

| Action | Gesture | Description |
| :--- | :--- | :--- |
| **Vertical Scroll** | 👌 **Pinch & Move Vertically** | Pinch Index & Thumb. Move UP/DOWN to scroll. |
| **Horizontal Scroll** | 👌 **Pinch & Move Horizontally** | Pinch Index & Thumb. Move LEFT/RIGHT to scroll. |

## 🔧 Troubleshooting

  * **Camera not opening:** Ensure no other application (Zoom, Teams) is using the camera. Check Windows Privacy settings to allow apps to access the camera.
  * **Controls not working:** Try running the script or terminal as Administrator. Some Windows API calls for volume/brightness require elevated privileges.
  * **Jittery Mouse:** Adjust lighting in your room. MediaPipe works best in well-lit environments.
  * **`ModuleNotFoundError: No module named 'mediapipe'`:** Ensure you are using a compatible Python version (3.10-3.12) and have activated your virtual environment.
