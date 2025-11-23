# Jute Fiber Variety Identification Using Deep Learning 
This project implements various deep learning models for classifying different varieties of jute fiber using microscopic and smartphone images.

## Dataset
The dataset used in this project is the "Jute Variety Dataset" which contains images of different jute fiber varieties:
-Bangladeshi White
-Tossa
-Mesta
-Kenaf

## Dataset Details
Total images: 4,906

## Imaging types:
-Microscopic images
-Smartphone images

SmartJute Dataset/
├── Bangladeshi_White/
│   ├── Microscope/
│   └── Smartphone/
├── Tossa/
│   ├── Microscope/
│   └── Smartphone/
├── Mesta/
│   ├── Microscope/
│   └── Smartphone/
└── Kenaf/
    ├── Microscope/
    └── Smartphone/

## Dataset Preprocessing:
All images resized to 122 × 122 × 3

Pixel values normalized to [0, 1]

Removed approximately 1,950 low-quality images

## Dataset split: 
80% training, 20% testing (random_state = 42)

## Data augmentation techniques:
-Rotation
-Zoom (up to 20%)
-Width & height shift
-Shearing
-Horizontal flipping

## Models Implemented

Microscopic Dataset:

-ResNet152V2 (Best Performer)
-EfficientNetV2S
-EfficientNetV2-B0

Smartphone Dataset:

-NASNetMobile (Best Performer)
-ResNet101V2
-MobileNetV3-Small

Combined Dataset:

-ResNet101V2 (Best Performer)
-ResNet152V2
-MobileNetV3-Large
-EfficientNetV2S
-ConvNeXtBase 

## Performance Metrics

Models were evaluated using:

-Accuracy
-Precision
-Recall
-F1 Score

| Dataset    | Best Model   | Accuracy | Precision | Recall | F1   |
| ---------- | ------------ | -------- | --------- | ------ | ---- |
| Microscope | ResNet152V2  | 92.42%   | 0.92      | 0.92   | 0.92 |
| Smartphone | NASNetMobile | 90%      | 0.90      | 0.90   | 0.90 |
| Combined   | ResNet101V2  | 89.41%   | 0.89      | 0.89   | 0.89 |

## System Architecture

The system includes:
-Deep learning models for classification.
-Web interface:
-FastAPI (Backend)
-Lovable (Frontend)
-Supabase (Authentication)

## Key Features

-Multi-variety classification
-Support for both microscope & smartphone images
-Automated preprocessing and augmentation
-Model performance visualization
-Confusion matrix and loss curve analysis
-Web-based prediction interface

## Acknowledgments

-Bangladesh Jute Research Institute (BJRI)
-Jute Products Development Centre (JPDC)
-Respective jute mills and contributors
-Open-source ML and AI communities

