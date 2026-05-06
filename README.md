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
```
## Install Dependencies

```bash
pip install mediapipe opencv-python scikit-learn numpy
```



## Run Training

Run the training notebook/script to:

- extract pose keypoints
- generate normalized features
- train the classifier
- save the trained model

Generated files:
- `pose_model.pkl`
- `label_encoder.pkl`

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
- webcam-based interaction

---

## Results

The system successfully:
- detects Surya Namaskar poses
- tracks sequence progression
- counts repetitions
- provides posture correction feedback
- detects incorrect pose order

Normalized pose keypoints and angle-based features significantly improved prediction stability and accuracy.

---

## Limitations

- Similar poses may occasionally be confused
- Requires proper lighting and full-body visibility
- Webcam support inside Google Colab is limited
- Form correction rules are manually designed

---

## Future Work

Possible future improvements include:

- Real-time deployment using Streamlit
- Voice-based yoga guidance
- Pose confidence scoring
- Mobile application support
- Deep learning based sequence models

---

## Team Members

- Keerthi Seela — 2023102012  
- Anumula Venkata Sai Sree Sahithi — 2023112002  
- Aditi Bose — 2023811005
