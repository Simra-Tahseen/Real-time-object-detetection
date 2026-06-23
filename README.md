# Real-Time Object Detection using YOLOv8 and OpenCV

## Overview

This project is a **real-time object detection system** built using **Python, OpenCV, and YOLOv8**.
It captures live video from the webcam, detects objects in each frame, draws bounding boxes around them, and displays the detected object names on the screen.

The project uses the **YOLOv8 pre-trained model** from the **Ultralytics** library for object detection and **OpenCV** for webcam access and visualization.

---

## Features

* Real-time object detection through webcam
* Uses **YOLOv8** pre-trained model
* Draws **bounding boxes** around detected objects
* Displays **object labels** on the video feed
* Prints detected object names in the terminal
* Simple and beginner-friendly Python implementation

---

## Technologies Used

* **Python**
* **OpenCV**
* **Ultralytics YOLOv8**

---

## Project Structure

```bash
object_detection_project/
│── main.py
│── requirements.txt
│── README.md
│── .gitignore
```

---

## How It Works

1. The webcam captures live video frames.
2. Each frame is passed to the **YOLOv8 model**.
3. The model detects objects and returns:

   * object class
   * confidence score
   * bounding box coordinates
4. If the confidence score is above the threshold, the object is displayed on the frame.
5. The processed frame is shown in a live window.

---

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Create and activate a virtual environment (optional but recommended)

#### Windows

```bash
python -m venv .venv
.venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the project

```bash
python main.py
```

---

## Sample Code Logic

The project loads the YOLO model and processes webcam frames like this:

* Open webcam using `cv2.VideoCapture(0)`
* Run YOLO model on each frame
* Extract detected object labels and confidence scores
* Draw bounding boxes and labels using OpenCV
* Show the result in a window

---

## Example Output

When the webcam is running, the application may detect objects such as:

* person
* bottle
* chair
* laptop
* cell phone
* book

The output window displays:

* a live webcam feed
* green bounding boxes around detected objects
* object names above each box

The terminal prints:

```bash
Detected objects: ['person', 'cell phone']
Detected objects: ['bottle']
```

---

## Supported Object Classes

The YOLOv8 model used in this project is pre-trained on the **COCO dataset**, which supports **80 object classes** such as:

* person
* car
* bicycle
* dog
* cat
* chair
* bottle
* laptop
* cell phone
* book
  and many more.

---

## Challenges Faced

* Some objects may be detected incorrectly if they look similar to another trained class.
* Small or unclear objects may not be recognized accurately.
* Detection accuracy depends on lighting, object visibility, webcam quality, and model size.

---

## Future Improvements

* Use a larger YOLO model such as **YOLOv8s / YOLOv8m** for better accuracy
* Add **object counting**
* Save detected frames or screenshots
* Detect only selected objects (for example: person, bottle, phone)
* Add voice output for detected objects
* Build a Streamlit or web interface for the project
* Train a **custom model** for specific objects

---

## Conclusion

This project demonstrates how **computer vision** and **deep learning** can be used together for real-time object detection.
It is a good beginner-level project to understand:

* webcam frame processing
* object detection using YOLO
* bounding box drawing with OpenCV
* integrating pre-trained AI models into Python applications

---

## Author

**Simra Tahseen**
