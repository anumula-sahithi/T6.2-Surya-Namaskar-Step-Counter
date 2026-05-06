# T6.2-Surya-Namaskar-Step-Counter

## Overview

This project is a computer vision and machine learning based yoga assistant for Surya Namaskar. The system detects yoga poses, checks the sequence of steps, counts repetitions, and provides basic form correction feedback.

The project uses MediaPipe Pose for human pose estimation and machine learning classifiers for pose recognition.

---

## Features

- Surya Namaskar pose detection
- 12 step sequence tracking
- Repetition counting
- Wrong pose detection
- Form correctness feedback
- Webcam and image based testing support


---

## Surya Namaskar Sequence

The complete Surya Namaskar cycle contains 12 steps:

1. Pranamasana
2. Hasta Uttanasana
3. Padahastasana or Uttanasana
4. Ashwa Sanchalanasana or Anjaneyasana
5. Chaturanga Dandasana
6. Ashtanga Namaskara
7. Bhujangasana
8. Adho Mukha Svanasana
9. Ashwa Sanchalanasana or Anjaneyasana
10. Padahastasana or Uttanasana
11. Hasta Uttanasana
12. Pranamasana

Although the sequence contains 12 steps, there are 8 distinct poses.

---

## Dataset

The dataset was created using images from the Kaggle dataset and additional manually collected images


[Google Drive Dataset](https://1drv.ms/f/c/1b8257c358f1efa1/IgAowFBipBqhRbbFDpyua8qBAWuquUvxYPi9PVtYqp5Z_-k?e=EoCSSI)

---

## Technologies Used

- Python
- OpenCV
- MediaPipe
- Scikit-learn
- NumPy
- Google Colab

---

## Methodology

1. Detect pose keypoints using MediaPipe Pose
2. Extract normalized landmark coordinates
3. Compute angle based features
4. Train machine learning classifier
5. Predict yoga pose
6. Validate Surya Namaskar sequence
7. Provide form correction feedback

---

## Model

The system uses a Multi Layer Perceptron (MLP) based machine learning approach for yoga pose classification. MediaPipe Pose is used to extract pose keypoints from the human body, after which normalized landmark coordinates and angle based geometric features are computed and used for pose prediction.

The predicted pose is further used for sequence tracking, repetition counting, wrong-pose detection, and form-correction feedback.

---
## Pose Detection

The system performs yoga pose detection using MediaPipe Pose estimation and machine learning based classification.

The pose detection pipeline includes
- Extraction of pose keypoints
- Landmark normalization
- Angle based feature computation
- Yoga pose prediction

The system is capable of recognizing Surya Namaskar related yoga poses from uploaded images and webcam input.

---

## Sequence Detection

The system validates the order of Surya Namaskar poses using a sequence tracking engine.

The sequence detection module performs:
- Step by step pose validation
- Repetition counting
- Incorrect pose order detection
- Next pose guidance

It tracks the complete 12 step Surya Namaskar flow while handling repeated poses and prediction noise.

---
## Form Correction

The system performs rule based form checks for different poses and gives feed back using following
- Knee angles
- Elbow angles
- Hip position
- Body alignment

---


## Install Dependencies

```bash
!pip install mediapipe==0.10.20 protobuf==4.25.3
```



## Run Training

Run the training notebook to:

- extract pose keypoints
- generate normalized features
- train the classifier

---

## Run Sequence Detection

Run the sequence detection notebook/script to:

- predict Surya Namaskar poses
- validate sequence order
- count repetitions
- detect incorrect poses
- provide form correction feedback

The system supports:
- uploaded image testing
- webcam based interaction

---

## Results

The developed system can detect Surya Namaskar poses, track sequence progression, count repetitions, identify incorrect pose order, and provide basic posture correction feedback. The use of normalized pose keypoints and angle based geometric features improved the prediction stability and pose recognition performance.

---

## Limitations

- Similar poses may occasionally be confused
- Requires proper lighting and full body visibility
- Webcam support inside Google Colab is limited

---

## Future Work

Possible future improvements include:

- Real time deployment using Streamlit
- Voice based yoga guidance
- Mobile application support
- Deep learning based sequence models




