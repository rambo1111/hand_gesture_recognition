# Gesture Recognition Dataset Collection

## collect_images

### Introduction

This repository contains a simple Python script for capturing frames to create a dataset for gesture recognition. The code uses OpenCV to access the webcam and capture a specified number of frames for each class of gestures.

### Prerequisites

Make sure you have the following installed before running the script:

- Python
- OpenCV (cv2)

You can install OpenCV using the following command:

```bash
pip install opencv-python
```

### Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/gesture-recognition-dataset.git
```

2. Navigate to the project directory:

```bash
cd gesture-recognition-dataset
```

3. Run the script:

```bash
python capture_dataset.py
```

4. Follow the on-screen instructions:

   - Enter the number of signs (classes) you want to capture.
   - Enter the number of frames to be captured per sign.

   The script will then prompt you to press "Q" when you are ready to start capturing frames.

### Directory Structure

The captured frames will be organized in the following directory structure:

```
- data
  - 0
    - 0.jpg
    - 1.jpg
    - ...
  - 1
    - 0.jpg
    - 1.jpg
    - ...
  - ...
```

Each subdirectory corresponds to a class (sign), and the frames for that class are saved as individual image files within the respective subdirectory.

### Notes

- Press "Q" to start capturing frames for each class.
- The webcam feed will be displayed, and frames will be saved on keypress.
- Press "Q" again to move to the next class.

### Acknowledgments

This code is a basic template for capturing a gesture dataset. Feel free to customize and extend it based on your specific requirements.