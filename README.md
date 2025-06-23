# Face Recognition with YOLOv8 + FaceNet

This project implements a face recognition pipeline using **YOLOv8** for face detection and **FaceNet** for face embeddings, followed by **SVM classification**. It is fully compatible with **Google Colab** and supports **Google Drive integration**.

---

## 🔍 Features

- ✅ Face detection using [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- ✅ Face embeddings using [FaceNet (VGGFace2)](https://github.com/timesler/facenet-pytorch)
- ✅ Classification using Scikit-learn SVM
- ✅ Accuracy: ~95–97% on real celebrity datasets
- ✅ Automatic fallback to dataset image if no test image is uploaded
- ✅ Confusion matrix visualization
- ✅ Google Drive storage and dataset extraction

---

## 📁 Directory Structure

face_recognition_project/

├── embeddings/

│   ├── face_embeddings.npy

│   └── labels.npy

├── models/

│   ├── svm_classifier.joblib

│   └── label_encoder.joblib

├── unzipped/

│   └── Dataset/

│       └── Person_A/

│           ├── image1.jpg

│           └── ...

├── Face_Recognition_Yolo_Facenet.ipynb



---

## 🚀 Getting Started (Google Colab)

Click the button below to launch the notebook in Colab:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

### Steps:

1. Mount your Google Drive.
2. Upload your dataset ZIP (structure: `Dataset/Person_Name/*.jpg`)
3. Run all cells to train and test.
4. Optionally upload your own test image, or the script picks one from the dataset.

---

## 📦 Dataset Format

Upload a ZIP file like this:

Dataset/

├── Person_1/

│   ├── image1.jpg

│   └── image2.jpg

├── Person_2/

│   ├── image1.jpg

│   └── image2.jpg


Recommended size: At least 5 images per class.

---

## 📊 Results

- Achieved accuracy of **97.3%** with RBF kernel SVM and raw FaceNet embeddings.
- Dataset: 5–10 celebrities with 10–30 images each.

---

## 🛠 Dependencies

Install automatically in Colab:

```bash
pip install ultralytics facenet-pytorch opencv-python scikit-learn matplotlib seaborn



✨ Acknowledgments

Ultralytics YOLOv8

facenet-pytorch

Scikit-learn

Google Colab
