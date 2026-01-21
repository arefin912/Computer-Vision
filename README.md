# 🧠 Computer Vision Project  
## People Detection, Tracking, Counting & Heatmap Visualization

This project demonstrates **end-to-end computer vision techniques** for detecting, tracking, counting people, and visualizing movement patterns from a video stream.  
It combines **object detection, multi-object tracking, in/out counting, and heatmap generation** using modern CV frameworks.

---

## 🚀 Project Overview

The system processes a video of people walking and performs:

- ✅ **Object Detection** (People detection)
- 🔁 **Multi-Object Tracking**
- ➕➖ **People In/Out Counting**
- 🔥 **Heatmap Visualization** for movement density

The outputs are annotated videos that clearly show detections, tracking IDs, counts, and heat intensity.

---

## ✨ Features

### 🔍 Object Detection
- Detects people in each video frame using **RFDETR**
- Bounding boxes and labels are added using **Supervision**

### 🧍‍♂️ People Tracking & Counting
- Uses **YOLOv8 + BoT-SORT tracker**
- Assigns unique IDs to individuals
- Counts people crossing predefined **“IN”** and **“OUT”** lines
- Prevents double counting using tracking history

### 🔥 Heatmap Generation
- Generates a color-coded heatmap overlay
- Red areas → high activity
- Blue areas → low activity
- Built using **Supervision HeatMapAnnotator**

---

## 🎥 Demo Outputs

The project generates the following videos:

- 📌 **Annotated Detection Video**  
  `annotated_video.mp4`
<img width="1440" height="809" alt="Screenshot 2026-01-22 at 4 17 15 am" src="https://github.com/user-attachments/assets/8445f867-0371-4cf2-b168-3407cfc86136" />

- 📌 **Tracking & Counting Video**  
  `output_counting.mp4`
<img width="1440" height="809" alt="Screenshot 2026-01-22 at 4 19 21 am" src="https://github.com/user-attachments/assets/f9154cdb-992b-4e8d-aaed-3ac0896afde4" />

- 📌 **Heatmap Visualization Video**  
  `output_heatmap.mp4`
<img width="1440" height="809" alt="Screenshot 2026-01-22 at 4 18 18 am" src="https://github.com/user-attachments/assets/224d21bf-f1f6-429f-9def-32ba12fc0469" />


---

## 🧰 Tech Stack

- **Python 3.8+**
- **YOLOv8** – Object detection & tracking
- **RFDETR** – Transformer-based object detection
- **Supervision** – Annotation & heatmap tools
- **OpenCV** – Video processing
- **NumPy**

---
## 📦 Requirements

Install required libraries using:

bash
pip install ultralytics supervision rfdetr opencv-python numpy pytesseract roboflow inference

## ▶️ Usage

### 1️⃣ Clone the repository
```bash
git clone https://github.com/arefin912/Computer-Vision.git
cd Computer-Vision
2️⃣ Open the notebook
Open people_walking.ipynb in:

Jupyter Notebook

Google Colab (recommended)

3️⃣ Run the notebook cells
Run the cells sequentially:

Dependency Installation

Object Detection

Generates annotated_video.mp4

People Tracking & Counting

Generates output_counting.mp4

Heatmap Generation

Generates output_heatmap.mp4

📹 Video Source
The default video is fetched from Roboflow:

https://media.roboflow.com/supervision/video-examples/people-walking.mp4
You can replace it with your own video by updating the video path in the notebook.

⚙️ How It Works
🔍 Detection
RFDETR predicts bounding boxes for people

Supervision annotates frames with labels and confidence

🔁 Tracking & Counting
YOLOv8 + BoT-SORT tracks people across frames

Virtual lines define IN and OUT zones

Directional movement determines entry or exit

🔥 Heatmap
Detection points accumulate over frames

Density is mapped using a color scale

Highlights high-traffic areas clearly

📊 Results
Accurate detection and tracking of individuals

Reliable people counting across defined zones

Clear visualization of foot traffic density

Output videos saved in the working directory

🙏 Credits
YOLOv8 – Ultralytics

RFDETR – Transformer-based detector

Supervision Library – Annotations & heatmaps

Video Source – Roboflow

Inspired by computer vision tutorials from Roboflow and Ultralytics

👤 Author
Md. Shams Arefin
🎓 CSE @ ULAB
🤖 AI Engineering | Computer Vision | Deep Learning

📫 Email: shams.arefin.cse@ulab.edu.bd
🔗 LinkedIn: https://www.linkedin.com/in/arefin99
