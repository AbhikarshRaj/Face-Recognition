# Face Recognition System using FaceNet

This project demonstrates how to build a face recognition system using the FaceNet model and associated tools. The system focuses on the **face identification** task, where we identify a given face by comparing it against a database of known faces.

## Table of Contents

- [Introduction](#introduction)
- [Setup and Installation](#setup-and-installation)
- [Project Workflow](#project-workflow)
  - [1. Face Detection](#1-face-detection)
  - [2. Face Embeddings](#2-face-embeddings)
  - [3. Face Classification](#3-face-classification)
  - [4. Prediction for Unseen Photos](#4-prediction-for-unseen-photos)
- [Resources](#resources)

## Introduction

Face recognition refers to the task of identifying or verifying individuals based on their facial features. The key aspects of this project are:

- **Face Verification**: A one-to-one comparison (Is this the person?).
- **Face Identification**: A one-to-many comparison (Who is this person?).

This system uses **FaceNet**, a face recognition model developed by Google, which converts face images into 128-dimensional embeddings. These embeddings are then used for classification and identification purposes.

## Setup and Installation

### 1. Install Required Packages

To begin, you need to install the required Python packages:

```bash
pip install mtcnn
pip install numpy
pip install scikit-learn
pip install keras
You can also create a requirements.txt file with the following content:

Copy code
mtcnn
numpy
scikit-learn
keras
2. Download Pre-Trained FaceNet Model
We will use a pre-trained FaceNet model provided by Hiroki Taniai. The model is trained on the MS-Celeb-1M dataset and expects input images to be 160x160 pixels and color-encoded.

Download Pre-trained FaceNet Model

Project Workflow
1. Face Detection
In this step, we use the MTCNN (Multi-Task Cascaded Convolutional Neural Network) model to detect faces in images. The MTCNN model identifies face bounding boxes and facial landmarks (such as eyes, nose, and mouth), which will be used for further analysis.

You can find the face detection code here:

face_detection.py

2. Face Embeddings
Face embeddings are vectors that represent the unique features of each face. These embeddings are extracted using the FaceNet model. Given an image of a face, the model produces a 128-dimensional vector that can be compared with other embeddings.

To extract face embeddings, use the code provided:

face_embeddings.py

3. Face Classification
Once we have the face embeddings, we use a Support Vector Machine (SVM) classifier to match and classify faces. The SVM model is trained on the embeddings and their corresponding labels.

You can find the face classification code here:

face_classification.py

4. Prediction for Unseen Photos
For making predictions, we will use the trained model to classify new, unseen images. This process involves detecting the face, generating the embedding, and then classifying it against the known identities.

Prediction code can be found here:

face_system.py

Resources
How to Develop a Face Recognition System using FaceNet in Keras and an SVM Classifier
FaceNet Paper by Google
Keras OpenFace Repository
FaceNet by David Sandberg
FaceNet by Hiroki Taniai
MS-Celeb-1M Dataset
MTCNN Paper
Linear Support Vector Machine (SVM)
5 Celebrity Faces Dataset on Kaggle
Contributing
If you would like to contribute to this project, feel free to fork the repository, create a new branch, and submit a pull request.

License
This project is licensed under the MIT License.

yaml
Copy code

---

### Key Changes:
- Updated the introduction and installation steps.
- Provided links to the code files and resources for better clarity.
- Organized the sections into a logical flow from setup to usage.

Let me know if you'd like any additional modifications!
