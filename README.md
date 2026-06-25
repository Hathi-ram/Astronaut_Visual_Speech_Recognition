# Astronaut_Visual_Speech_Recognition
Real-Time Astronaut Command Recognition Through Transfer Learning-Based Automatic Lip Reading using MediaPipe, MobileNetV2, BiLSTM, and CTC Loss.

# Real-Time Astronaut Command Recognition Through Transfer Learning-Based Automatic Lip Reading

## Overview

This project presents a Visual Speech Recognition (VSR) system for astronaut command recognition using automatic lip reading techniques.

The proposed framework recognizes spoken commands directly from lip movements without relying on audio signals. The system combines MediaPipe Face Mesh, MobileNetV2 transfer learning, Bidirectional LSTM networks, and CTC decoding to predict command-oriented speech from silent video sequences.

---

## Problem Statement

Communication is a critical aspect of astronaut missions. Audio-based communication systems may be affected by environmental noise, signal degradation, equipment failures, or communication delays.

To address this challenge, this project explores visual speech recognition as an alternative communication method by recognizing spoken commands from lip movements alone.

---

## Dataset

**GRID Corpus**

The GRID corpus contains structured command-oriented sentences that are suitable for visual speech recognition tasks.

Example Commands:

* Place blue in B seven soon
* Set green at C five again
* Lay red with F two please

Dataset Structure:

Command + Color + Preposition + Letter + Digit + Adverb

---

## Methodology

### 1. Mouth Region Extraction

* Face detection using MediaPipe Face Mesh
* Lip landmark localization
* Mouth Region of Interest (ROI) extraction

## 

### 2. Preprocessing

* Grayscale conversion
* Histogram equalization
* Image normalization
* Frame resizing
* Sequence padding to 75 frames

### 3. Feature Extraction

* MobileNetV2 (Transfer Learning)
* Pretrained ImageNet weights
* Spatial feature extraction

### 4. Temporal Modeling

* Bidirectional LSTM Networks
* Sequence learning from video frames

### 5. Sequence Prediction

* Connectionist Temporal Classification (CTC) Loss
* Text decoding

---
## <img width="1730" height="666" alt="frame vs mouth" src="https://github.com/user-attachments/assets/ba545191-edf9-48e8-96ff-a3dc13ea2df3" />


## Model Architecture

Video Input

↓

Mouth ROI Extraction

↓

Preprocessing

↓

MobileNetV2

↓

BiLSTM

↓

CTC Decoder

↓

Predicted Command

---

## Performance Results

| Metric                     | Value  |
| -------------------------- | ------ |
| Character Accuracy         | 85.77% |
| Word Accuracy              | 69.67% |
| Character Error Rate (CER) | 14.23% |
| Word Error Rate (WER)      | 36.33% |

---

## Sample Predictions

| Actual                     | Predicted                 |
| -------------------------- | ------------------------- |
| place red in v four now    | place red in v four now   |
| place blue in b seven soon | place blue in p seven son |
| set green at c five again  | set gren at five again    |
| set white in h seven soon  | set white in seven son    |

---

## Technologies Used

* Python
* TensorFlow
* Keras
* OpenCV
* MediaPipe
* NumPy
* Pandas
* Matplotlib
* Streamlit

---

## Project Structure

Astronaut_Visual_Speech_Recognition/

├── notebook/

├── models/

├── results/

├── paper/

├── dataset/

├── app.py

├── requirements.txt

└── README.md

---

## Dataset Availability

The GRID corpus dataset is not included in this repository due to size limitations.

Dataset can be downloaded from:

https://spandh.dcs.shef.ac.uk/gridcorpus/

---

## Future Work

* Transformer-based Visual Speech Recognition
* Larger Vocabulary Recognition
* Real-Time Deployment
* Edge Device Optimization
* Multilingual Command Recognition

---

## Author

**Vislavath Hathiram**

B.Tech Smart Manufacturing Engineering

Indian Institute of Information Technology, Design and Manufacturing (IIITDM) Kancheepuram

---

## License

This project is intended for academic and research purposes.
