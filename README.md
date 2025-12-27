
# Facial-Expression-Intelligence-System

A real-time face-emotion detection heads-up display (HUD) built with **OpenCV** and **DeepFace**. The application analyzes facial expressions from a webcam feed and visualizes the top detected emotion along with confidence bars for all tracked emotions.

## Features

* Real-time webcam emotion detection
* Supports five emotions: `angry`, `happy`, `sad`, `surprise`, `neutral`
* Clean HUD interface with:

  * Central face-tracking box
  * Top emotion label with confidence
  * Side emotion bar panel
* Smooth performance with timed analysis interval
* Works even when no face is detected (fallback values)

## Tech Stack

* Python
* OpenCV
* DeepFace
* TensorFlow (backend dependency)

## Installation

1. Clone the repository

```bash
git clone https://github.com/Sk-Sharief/Facial-Expression-Intelligence-System.git
cd <Facial-Expression-Intelligence-System>
```

2. Create and activate a virtual environment (recommended)

```bash
python -m venv venv
venv\Scripts\activate   # Windows
# or
source venv/bin/activate   # Mac/Linux
```

3. Install dependencies

```bash
pip install opencv-python deepface tensorflow
```

*(TensorFlow may take time depending on your system.)*

## Usage

Run the main script:

```bash
python project.py
```

Controls:

* Press **`q`** to exit

## Project Structure

```
.
├── project.py        # Main application
├── README.md
└── assets/           # (Optional) screenshots or demo images
```

## Screenshots

Sad:

<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/766597af-a4f0-4407-a581-6242c5b6013e" />

Neutral:

<img width="1919" height="1079" alt="Screenshot 2025-12-27 115627" src="https://github.com/user-attachments/assets/2c481463-3256-4216-a935-d0e3b83021a8" />


## How It Works

1. Captures frames from the webcam using OpenCV
2. Runs DeepFace emotion analysis every few milliseconds
3. Extracts probabilities for five target emotions
4. Displays:

   * Highest-confidence emotion
   * Confidence bars for all emotions
5. Renders UI overlays using OpenCV drawing APIs

## Configuration

You can tweak the following inside the script:

* Frame analysis interval
* Bar spacing and UI layout
* Tracked emotions list

```python
ANALYZE_EVERY = 0.2
EMOTIONS = ["angry", "happy", "sad", "surprise", "neutral"]
```

## Limitations

* Accuracy depends on lighting and camera quality
* Works best with a single face in frame
* TensorFlow CPU mode may be slower on low-end systems

## Future Enhancements

* Full-screen HUD mode
* FPS optimization
* Face-tracking box animation
* Export emotion logs to CSV
* Multi-face support

## Credits

* OpenCV
* DeepFace Framework
* TensorFlow

## License

MIT License

