# Hand Gesture Recognition

### Introduction

This project is designed to capture hand gestures through a webcam, create a dataset for training a machine learning model, train a Random Forest classifier to recognize these gestures, and finally, deploy a Flask web application that performs real-time hand gesture recognition. The entire workflow is divided into four key scripts: collecting data (collect_imgs.py) dataset creation (create_dataset.py), model training (train_classifier.py), and web application deployment (app.py) in project directory, which utilizes a pre-trained model saved in model.p.



### Prerequisites

Make sure you have the following installed before running the scripts:

- Python
- OpenCV (cv2)
- mediapipe
- scikit-learn
- Numpy
- Flask

You can install prerequisites using the following command:

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

3. Run thi script:

```bash
python collect_imgs.py
```

4. Follow the on-screen instructions:

   - Enter the number of signs (classes) you want to capture.
   - Enter the number of frames to be captured per sign.
   - when camera starts put your hand out and show it to camera, just bring back and forth your hand to record your data
   - repeat the steps with different hand styles.

   The script will then prompt you to press "Q" when you are ready to start capturing frames.

5. Now run this script:

```bash
python create_dataset.py
```
This will create a binary file data.pickle

6. Now run this script:

```bash
python train_classifier.py
```
This will create the model name model.p

7. Now open project folder and run app.py. 

   - You will see labels_dict variable, but it should be empty 
   ![labels_dict](https://github.com/rambo1111/hand_gesture_recognition/blob/main/image.png)
   - Customize your labes_dict like this, number keys is equal to number_of _classes and values is the name of hand symbol you are showing there. 

8. You can also run interference_classifier but it has some bugs currently, you need to install this package before running it.

```bash
pip install pyttsx3
```

```bash
python interference_classifier.py
```

### Directory Structure

Data directory will be created after executing (collect_imgs.py) 
The captured frames will be organized in the data directory :

```
- code
  - collect_imgs.py
  - create_dataset.py
  - interference_classifier.py (this file is under development)
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

### Notes

- Press "Q" to start capturing frames for each class.
- The webcam feed will be displayed, and frames will be saved on keypress.
- Press "Q" again to move to the next class.
- Make sure your image files are organized in the `./data` directory with subdirectories representing different classes.
- The script utilizes the MediaPipe library to extract hand landmarks, and it assumes that images contain hands with sufficient visibility.
- Ensure that the data.pickle file is present in the project directory.
- The script uses the scikit-learn library for training and evaluating the Random Forest classifier.
- You can adjust the test_size parameter in the train_test_split function to modify the training/testing split ratio.
- The app uses the model.p file to load the pre-trained Random Forest classifier.
- The mediapipe library is used to detect hand landmarks, and the results are overlaid on the video feed.
- The predicted hand gesture is displayed in real-time on the web interface.

### Remark

Feel free to customize the scripts based on your specific requirements. You can modify the dataset creation process, experiment with different classifiers, or integrate additional features for a more robust hand gesture recognition system

## Issues and Contributions

If you encounter any issues or would like to contribute to the project, please open an issue or submit a pull request on the GitHub repository.