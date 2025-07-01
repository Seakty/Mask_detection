<div align="center">

# 🚀 Real-Time Face Mask Detection with YOLOv12 😷

A high-performance, real-time system to accurately detect face masks in images, videos, and live camera streams.

<p>
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/Framework-PyTorch-orange.svg" alt="PyTorch">
  <img src="https://img.shields.io/badge/Model-YOLOv12-purple.svg" alt="YOLOv12">
  <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
</p>

</div>

![image](https://github.com/user-attachments/assets/ce2e8f43-237a-44ab-a680-a53de0cf0660)


> This project can identify if a person is wearing a mask or not at all, making it suitable for monitoring compliance in public spaces.

---

## 📋 Table of Contents

- [✨ Features](#-features)
- [📂 File Descriptions](#-file-descriptions)
- [🏁 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [▶️ Usage](#️-usage)
  - [Command-Line Arguments](#command-line-arguments)
  - [Examples](#examples)
- [🧠 Model Training](#-model-training)
- [⌨️ Runtime Controls](#️-runtime-controls)
- [🧑‍💻 Contributors](#-contributors)
- [📜 License](#-license)

---

## ✨ Features

* **🎯 High Accuracy:** Utilizes a custom-trained YOLOv12 model for precise and reliable detection.
* **⚡ Real-Time Performance:** Capable of processing video streams and webcam feeds with minimal latency.
* **🔌 Versatile Input:** Supports various input sources:
    * Single images (`.jpg`, `.png`)
    * Folders of images
    * Video files (`.mp4`, `.avi`)
    * Live webcam feeds
* **🔧 Customizable:** Easily adjust the detection confidence threshold and output resolution.
* **📹 Recording Capability:** Option to record and save the output with bounding boxes.

---

## 📂 File Descriptions

* `yolo_detect.py`: 🐍 The main Python script to run the face mask detection.
* `my_model_v12.pt`: 🤖 The pre-trained YOLOv12 model weights.
* `requirements.txt`: 📦 A list of the necessary Python libraries for the project.
* `Real-Time Face Mask Detection Using YOLOv12.pdf`: 📄 A detailed document about the project.
* `.gitignore`: ⚙️ Specifies files for Git to ignore.
* `yolo12s_run1/`: 📈 Directory containing training runs and results.

---

## 🏁 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

* Python 3.8 or later
* Pip (Python package installer)
* OpenCV

### Installation

1.  **Clone the repository:**
    ```sh
    git clone git@github.com:Seakty/Mask_detection.git
    cd Mask_detection
    ```

2.  **Create and activate a virtual environment:**
    * This keeps your project dependencies isolated.

    * **On macOS/Linux:**
        ```sh
        python3 -m venv venv
        source venv/bin/activate
        ```

    * **On Windows:**
        ```sh
        python -m venv venv
        .\venv\Scripts\activate
        ```

3.  **Install the required libraries:**
    * With your virtual environment activated, install the packages.
    ```sh
    pip install -r requirements.txt
    ```

---

## ▶️ Usage

The `yolo_detect.py` script is used from the command line to perform detection.

### Command-Line Arguments

| Argument       | Description                                                                                             | Required | Default |
| :------------- | :------------------------------------------------------------------------------------------------------ | :------: | :------ |
| `--model`      | Path to the YOLO model file (e.g., `my_model_v12.pt`).                                                   | **Yes** | `None`  |
| `--source`     | Input source: image path, video path, or webcam index (`usb0`).                                         | **Yes** | `None`  |
| `--thresh`     | Minimum confidence threshold for detection.                                                             |    No    | `0.5`   |
| `--resolution` | Display resolution in `WxH` format (e.g., `640x480`).                                                    |    No    | `None`  |
| `--record`     | A flag to record the output from a video or webcam feed.                                                |    No    | `False` |

### Examples

**🖼️ Detecting from a single image:**
```sh
python yolo_detect.py --model my_model_v12.pt --source path/to/your/image.jpg
```
🔴**Detecting from a video:**
```sh
python yolo_detect.py --model my_model_v12.pt --source path/to/your/video.mp4 --resolution 1280x720
```
💻 **Detecting with the realtime webcam:**
```sh
python yolo_detect.py --model my_model_v12.pt --source usb0 --resolution  1280x720
```
## 🧠 Training

he YOLOv12 model was trained on a custom dataset using Google Colab. If you are interested in the training process, dataset preparation, or want to train your own model, you can access the complete notebook.

https://colab.research.google.com/drive/1VvrWUryRJoPFhqQIA24nsxKmH0OYfYSz?usp=sharing

### 📜 License
This project is licensed under the MIT License.
