# T6.2-Surya-Namaskar-Step-Counter

## Overview

This project is a computer vision and machine learning based yoga assistant for Surya Namaskar. The system detects yoga poses, validates the sequence of steps, counts repetitions, and provides basic form-correction feedback.

The project uses MediaPipe Pose for human pose estimation and machine learning classifiers for pose recognition.

---

## Features

- Surya Namaskar pose detection
- 12-step sequence tracking
- Repetition counting
- Wrong pose detection
- Form correctness feedback
- Webcam and image-based testing support
- MediaPipe based pose keypoint extraction
- Machine learning based pose classification

---

## Surya Namaskar Sequence

The complete Surya Namaskar cycle contains 12 steps:

1. Pranamasana
2. Hasta Uttanasana
3. Padahastasana
4. Ashwa Sanchalanasana
5. Chaturanga Dandasana
6. Ashtanga Namaskara
7. Bhujangasana
8. Adho Mukha Svanasana
9. Ashwa Sanchalanasana
10. Padahastasana
11. Hasta Uttanasana
12. Pranamasana

Although the sequence contains 12 steps, there are 8 distinct poses.

---

## Dataset

The dataset was created using:
- Images from the Kaggle Yoga Pose Classification Dataset by Shruti Saxena
- Additional manually collected images

The original Kaggle dataset contains 47 yoga poses. A subset of Surya Namaskar related poses was selected for this project.

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
3. Compute angle-based features
4. Train machine learning classifier
5. Predict yoga pose
6. Validate Surya Namaskar sequence
7. Provide form-correction feedback

---

## Model

The project experiments with:
- Multi-Layer Perceptron (MLP)
- Random Forest Classifier

Random Forest provided more stable predictions and better performance.

---

## Form Correction

The system performs rule-based form checks for different poses using:
- Knee angles
- Elbow angles
- Hip position
- Body alignment

Example feedback:
- Keep knees straight
- Lift chest upward
- Raise hips higher

---

## Project Structure

```text
project/
│
├── dataset/
├── pose_model.pkl
├── label_encoder.pkl
├── training.ipynb
├── sequence_engine.ipynb
├── webcam_demo.ipynb
├── README.md
