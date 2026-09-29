# Facial Recognition for Automated Attendance Using CCTV Footage

A deep learning-based facial recognition system developed as an MSc final project at the University of Salford. The project explores automated attendance using CCTV-style footage through face detection, facial recognition, identity matching, and timestamp logging.

## Project Overview

This project investigates how facial recognition can be used to automate attendance recording without requiring manual input from users.

The system processes facial images or CCTV-style footage, detects faces, generates facial embeddings, compares them against a gallery of known identities, and records recognised individuals with attendance information.

The project focuses on two deep metric learning approaches:

* FaceNet
* ArcFace

ArcFace was used for facial embedding generation and identity matching using cosine similarity.

## Objectives

* Develop an automated facial recognition attendance system.
* Detect faces from CCTV-style input.
* Generate facial embeddings for identity representation.
* Match detected faces against known identities.
* Record recognised identities and timestamps.
* Evaluate recognition performance using standard classification metrics.
* Investigate performance across different datasets and demographic groups.
* Identify limitations affecting real-world facial recognition performance.

## System Workflow

```text
CCTV / Image Input
        ↓
Face Detection
        ↓
Face Preprocessing
        ↓
Facial Embedding Generation
        ↓
Identity Matching
        ↓
Cosine Similarity
        ↓
Identity / Unknown Prediction
        ↓
Attendance Recording
        ↓
Timestamp & Confidence Information
```

## Technologies Used

* Python
* OpenCV
* FaceNet
* ArcFace
* Scikit-learn
* Computer Vision
* Deep Learning
* Facial Embeddings
* Cosine Similarity

## Datasets

The project evaluated the facial recognition system using:

* Labeled Faces in the Wild (LFW)
* YouTube Faces Database
* FairFace

These datasets were used to investigate recognition performance, video-based testing, and demographic fairness.

## Recognition Approach

The system uses facial embeddings to represent individual faces as numerical feature vectors.

ArcFace embeddings were compared using cosine similarity to determine the closest identity within the known-face gallery.

A similarity threshold was used to determine whether a detected face should be recognised as a known individual or classified as **Unknown**.

## Attendance Logging

The system records attendance information for recognised individuals, including:

* Identity
* Timestamp
* Camera ID
* Prediction confidence information

This provides an automated approach to attendance recording and improves traceability compared with manual attendance processes.

## Model Evaluation

The recognition system was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

The confusion matrix was used to compare actual identities against predicted identities and analyse classification performance across individuals.

## Key Findings

The system demonstrated effective recognition under controlled testing conditions, particularly for individuals already represented in the known-face gallery.

The evaluation also identified limitations when conditions changed, including:

* Different lighting conditions
* Changes in facial expressions
* Changes in body position
* Input image quality
* Recognition of unseen individuals
* Dataset-specific input formats

The YouTube Faces Database also required a frame-based simulation approach because the available video data was not directly compatible with the intended OpenCV processing workflow.

## Limitations

The system has limited ability to generalise to individuals who are not represented in the existing identity gallery.

Performance can also vary depending on environmental and input conditions. The testing therefore does not represent every real-world CCTV scenario.

The project also found that different datasets can require modifications to the processing pipeline.

## Future Work

Potential future improvements include:

* Improving recognition of unseen individuals.
* Testing with larger and more diverse identity galleries.
* Improving robustness under changing lighting and pose conditions.
* Supporting more realistic continuous CCTV video processing.
* Further investigation of demographic fairness.
* Optimising the system for real-world deployment environments.

## Project Context

**Degree:** MSc Internet of Things with Data Science
**University:** University of Salford, Manchester, UK
**Project Type:** MSc Final Project
**Focus:** Computer Vision, Deep Learning, Facial Recognition and Automated Attendance

## Author

**Leonard George**

MSc Internet of Things with Data Science
University of Salford
