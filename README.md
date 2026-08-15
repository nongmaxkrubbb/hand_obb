# Retrolens - Hand Tracking Filter & Portal

An interactive camera filter application using hand tracking with MediaPipe and OpenCV. You can create a "portal" with your fingers which will apply various interesting filters (Mono, Dual-Tone, Pixelate, Invert, Sepia, Blur, Thermal, Sketch, Glitch, Neon, Galaxy).

## System Requirements
- Python 3.7 or newer
- Webcam

## How to Install and Run

### 1. Clone Repository
First, clone this repository to your computer and navigate to the folder (replace the URL with your GitHub repository link):
```bash
git clone <YOUR_GITHUB_URL>
cd <REPO_FOLDER_NAME>
```

### 2. Create Virtual Environment (Optional but Highly Recommended)
Use a virtual environment so that dependencies (libraries) do not conflict with other Python projects on your computer.
```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
Install all required Python libraries by running the following command:
```bash
pip install -r requirements.txt
```

Or if you want to install them manually one by one:
```bash
pip install opencv-python mediapipe numpy
```

### 4. Ensure MediaPipe Models are Available
This application requires two model files from MediaPipe which should already be inside this repository:
1. `hand_landmarker.task` (For detecting points on the hand)
2. `selfie_segmenter.tflite` (For Galaxy filter / separating background)

If the files are missing, make sure to place them in the same folder as the `main.py` file.

### 5. Run the Application
Run the main script by typing:
```bash
python main.py
```
*(Use `python3 main.py` if you are using macOS/Linux and not using a virtual environment)*

## How to Use Features

- **Opening a Portal:** Use the tips of the index finger and thumb from **both** of your hands in front of the camera (total 4 fingers). A rectangular portal will be formed between your four fingers, and the filter effect will appear inside it.
- **Changing Filter:** There are several ways to change the active filter:
  - Touch/bring close the tips of your thumb and pinky finger.
  - Or, bring close the tips of the index fingers from both of your hands.
- **Closing the Application:** Ensure the camera/Retrolens window is active (clicked), then press the **`q`** key on your keyboard to exit the application.

---
**Note:** Ensure the room has sufficient lighting so the hand detection from the camera can work optimally.  