## How It Works

### Step 1 — Training the Faces
The system first reads images from the `Images/` folder.

Each person's face is processed using the `face_recognition` library to extract unique 128-dimensional facial encodings.

These encodings are stored inside a serialized file (`encodings.pickle`) for fast real-time inference.

---

### Step 2 — Loading User Information
User-related information such as:
- Name
- Skills
- Occupation
- College
- Additional metadata

is loaded from `Details.json`.

---

### Step 3 — Real-Time Webcam Detection
The webcam stream is captured using OpenCV.

For performance optimization:
- Frames are resized to 0.25x scale
- RGB conversion is applied
- Face locations are detected in real time

---

### Step 4 — Face Recognition
The detected face encodings are compared with stored encodings using Euclidean distance matching.

If a match is found:
- The user's identity is verified
- Information is dynamically displayed on screen

If no match is found:
- The system labels the user as Unknown

---

### Step 5 — Futuristic HUD Overlay
A custom HUD-style interface overlays:
- Bounding boxes
- Animated scan effects
- User information panel
- Real-time detection feedback

This creates an Iron Man-inspired AI surveillance experience.
## Learning Outcomes

Through this project, I explored:
- Computer Vision
- Real-Time AI Systems
- Face Recognition Pipelines
- OpenCV Optimization
- Human-Computer Interaction
- Intelligent UI Design