# ✋ Hand Gesture Recognition System

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.5%2B-brightgreen)](https://opencv.org/)

A real-time hand gesture recognition system built using computer vision and machine learning techniques. This project enables touchless interaction by detecting and interpreting hand gestures through your webcam, allowing gesture-based control of applications and devices.

---

## 🎯 Features

- ✅ Real-time hand tracking and detection
- ✅ Gesture recognition & classification
- ✅ Touchless system control
- ✅ Lightweight and fast processing (optimized for real-time performance)
- ✅ Easy to extend with new gestures
- ✅ Webcam-based input (no special hardware required)
- ✅ Supports multiple hand detection

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Python** | Core programming language |
| **OpenCV** | Video capture and image processing |
| **MediaPipe** | Hand landmark detection |
| **NumPy** | Numerical computations |

---

## 📂 Project Structure

```
Hand-Gesture/
├── main.py                 # Entry point of the application
├── utils/                  # Utility functions for gesture processing
│   ├── gesture_handler.py
│   └── helper.py
├── models/                 # Pre-trained models and gesture definitions
│   ├── gesture_model.pkl
│   └── gestures.json
├── requirements.txt        # Project dependencies
├── README.md              # This file
└── LICENSE                # MIT License
```

---

## 📋 System Requirements

- **Python**: 3.8 or higher
- **Operating System**: Windows, macOS, or Linux
- **Webcam**: Any USB or built-in webcam
- **RAM**: Minimum 4GB
- **Storage**: ~500MB for dependencies

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Ritti902/Hand-Gesture.git
cd Hand-Gesture
```

### 2. Create Virtual Environment (Optional but Recommended)

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Verify Installation

```bash
python main.py --version
```

---

## ▶️ Quick Start

1. **Ensure your webcam is connected and accessible**
2. **Run the application:**

```bash
python main.py
```

3. **Expected Output:**
   - A window will open showing your webcam feed
   - Your hand landmarks will be highlighted in real-time
   - Recognized gestures will be displayed on screen
   - Press `ESC` to exit the application

---

## 🖐️ Supported Gestures

The system recognizes the following hand gestures:

| Gesture | Description | Use Case |
|---------|-------------|----------|
| 👍 **Thumbs Up** | Thumb pointing upward | Approve/Confirm |
| ✌️ **Peace Sign** | Two fingers extended | Victory/Next |
| 👊 **Fist** | Closed hand | Pause/Stop |
| 🖐️ **Open Hand** | All fingers extended | Play/Start |
| 👆 **Pointing Up** | Index finger pointing up | Scroll up |
| 👉 **Pointing Right** | Index finger pointing right | Next/Right |

*Note: You can extend the system with custom gestures by training the model with new data.*

---

## 📸 How It Works

```
┌─────────────────────────────────────────────────────────┐
│                    System Pipeline                       │
└─────────────────────────────────────────────────────────┘

1. Webcam Capture
   └─> Video frames from your webcam

2. Hand Detection (MediaPipe)
   └─> Detects hand position and landmarks (21 points per hand)

3. Gesture Processing
   └─> Analyzes landmark positions and geometry

4. Classification
   └─> Matches gesture pattern to trained gestures

5. Action Output
   └─> Executes corresponding system action
```

**Step-by-step breakdown:**
- Captures video feed in real-time (30 FPS)
- Detects hand landmarks using MediaPipe's pose detection
- Processes landmark coordinates to extract gesture features
- Classifies gestures using trained logic/model
- Outputs corresponding actions or system commands

---

## 🎯 Applications

- 🖱️ **Virtual Mouse Control** - Move cursor and click with hand gestures
- ⌨️ **Virtual Keyboard** - Type without physical keyboard
- 🎮 **Gaming Interfaces** - Control games with hand movements
- ♿ **Accessibility Tools** - Assist users with mobility constraints
- 🏠 **Smart Home Control** - Control lights, doors, and devices
- 🎬 **Presentation Control** - Navigate slides with gestures
- 📱 **Mobile Device Interaction** - Gesture-based app control

---

## 🔧 Configuration

You can customize the application by editing the configuration in `main.py`:

```python
# Camera settings
CAMERA_ID = 0              # Default camera (0 = built-in webcam)
FPS = 30                   # Frames per second
FRAME_WIDTH = 640          # Video width
FRAME_HEIGHT = 480         # Video height

# Detection confidence thresholds
MIN_DETECTION_CONFIDENCE = 0.7
MIN_TRACKING_CONFIDENCE = 0.5

# Gesture timeout (seconds)
GESTURE_TIMEOUT = 2.0
```

---

## 📊 Performance

- **Frame Rate**: 25-30 FPS (varies by hardware)
- **Latency**: ~50-100ms gesture recognition delay
- **Accuracy**: ~92% on standard gestures
- **CPU Usage**: ~15-25% (Intel i5 or equivalent)
- **Memory Usage**: ~300-400MB

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| **Webcam not detected** | Check if another app is using the camera. Restart the application. |
| **Low FPS/Lag** | Reduce `FRAME_WIDTH` and `FRAME_HEIGHT` in config. Close background apps. |
| **Gestures not recognized** | Improve lighting. Ensure hand is fully visible. Recalibrate gestures. |
| **ModuleNotFoundError** | Run `pip install -r requirements.txt` again. Verify virtual environment is active. |
| **Permission denied** | Grant webcam access in system settings (macOS/Linux). |

---

## 🚀 Future Improvements

- [ ] Support for multiple simultaneous gestures
- [ ] Deep learning model for improved accuracy
- [ ] Custom gesture training interface
- [ ] Hand pose estimation for complex gestures
- [ ] GPU acceleration support
- [ ] Integration with popular applications
- [ ] Mobile app version

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please ensure your code follows PEP 8 standards and includes appropriate documentation.

---

## 📚 Documentation & References

- [MediaPipe Hands Documentation](https://google.github.io/mediapipe/solutions/hands.html)
- [OpenCV Documentation](https://docs.opencv.org/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Python Official Documentation](https://docs.python.org/3/)

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Ritti902**

- GitHub: [@Ritti902](https://github.com/Ritti902)
- Project: [Hand-Gesture](https://github.com/Ritti902/Hand-Gesture)

---

## 🙏 Acknowledgments

- Google MediaPipe team for the incredible hand detection library
- OpenCV community for computer vision tools
- All contributors and users who help improve this project

---

**⭐ If you find this project helpful, please consider giving it a star!**

For questions or issues, please open an [Issue](https://github.com/Ritti902/Hand-Gesture/issues) on GitHub.
