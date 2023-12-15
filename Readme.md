# Hand Gesture Recognition

### Introduction

This project is designed to capture hand gestures through a webcam, create a dataset for training a machine learning model, train a Random Forest classifier to recognize these gestures, and finally, deploy a Flask web application that performs real-time hand gesture recognition. The entire workflow is divided into four key scripts: collecting data ('collect_imgs.py') dataset creation ('create_dataset.py;), model training ('train_classifier.py'), and web application deployment ('app.py') in project directory, which utilizes a pre-trained model saved in model.p.



### Prerequisites

Make sure you have the following installed before running the script:

- Python
- OpenCV (cv2)
- mediapipe
- scikit-learn
- Numpy
- Flask

You can install OpenCV using the following command:

```bash
pip install opencv-python
pip install Flask
pip install numpy
pip install scikit-learn
pip install mediapipe

```

### Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/hand_gesture_recognition.git
```

2. Navigate to the project directory:

```bash
cd hand_gesture_recognition
```

3. Run the script:

```bash
python collect_imgs.py
```

4. Follow the on-screen instructions:

   - Enter the number of signs (classes) you want to capture.
   - Enter the number of frames to be captured per sign.

   The script will then prompt you to press "Q" when you are ready to start capturing frames.

5. Now run the script:

```bash
python create_dataset.py
```

### Directory Structure

The captured frames will be organized in the following directory structure:

```
- code
  - collect_imgs.py
  - create_dataset.py
  - interference_classifier.py <!-- this file is under development -->
  - train_classifier.py

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

 - project
   - static
     - style.css
   - template
     - html.css
   - app.py
```

Each subdirectory corresponds to a class (sign), and the frames for that class are saved as individual image files within the respective subdirectory.

### Notes

- Press "Q" to start capturing frames for each class.
- The webcam feed will be displayed, and frames will be saved on keypress.
- Press "Q" again to move to the next class.

### Acknowledgments

This code is a basic template for capturing a gesture dataset. Feel free to customize and extend it based on your specific requirements.