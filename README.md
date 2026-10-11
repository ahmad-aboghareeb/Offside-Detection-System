# Offside-Detection-System
A computer-vision system for automatic offside detection in football (soccer).  
The project detects players and the ball, maps image coordinates to pitch coordinates (via camera calibration / homography), tracks relevant players, and applies offside logic to determine and visualize offside events.
---
Features
🎯 Player and ball detection (object detection model or background-subtraction + heuristics).
🔗 Camera calibration & homography: maps image points to field (pitch) coordinates.
🧭 Player tracking across frames (simple tracking or advanced multi-object tracker).
📏 Offside decision logic using projected positions and the last-defender rule.
🎥 Visualization: draw detection boxes, pitch projection, offside line, and annotate frames.
💾 Optional: save annotated video / export events (timestamps, frame indices).
---
Requirements
> Adjust the commands below depending on whether your implementation is in **Python** or **C++**.
Common
A recorded match video or live feed (camera).
Reasonable camera view of the pitch and calibration data (or known pitch markers).
Python (typical)
Python 3.8+
OpenCV (`opencv-python`)
NumPy
[Optional] Deep learning framework: PyTorch or TensorFlow (if using trained detection models).
[Optional] `torchvision`, `opencv-contrib-python` (for tracking/extra algorithms).
Install example (Python):
```bash
python -m venv venv
source venv/bin/activate        # Linux / macOS
venv\Scripts\activate           # Windows

pip install -r requirements.txt
# or minimal
pip install opencv-python numpy
