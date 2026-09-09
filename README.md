# Automated Bender-Gestalt Figure Analysis Using Computer Vision

## Goal

Detect the nine Bender-Gestalt figures and identify drawing difficulties such as fragmentation, closure problems, rotation, curvature and angle changes, intersections, simplification, and overlap.

## Role

Developed the image-processing pipeline, YOLOv8 object-detection model, feature-extraction algorithms, and evaluation workflow.

## Method

- Preprocess grayscale scans using adaptive thresholding and connected-component filtering.
- Train YOLOv8 to detect and crop the nine figures.
- Compare student drawings with reference templates using eight Gestalt-based algorithms.
- Evaluate the model using training, validation, and test image splits.

## Result

The YOLOv8 detector achieved approximately 91.9% precision, 92.2% recall, 95.1% mAP@50, and 74.5% mAP@50-95 at the final training epoch. The system produced figure crops and automated indicators of drawing difficulties for the Bender-Gestalt cases.

## Source Label

Training dataset: scanned Bender-Gestalt drawings from a school-age participant sample. The repository does not document a verified client, volunteer, or practice classification.

## Evidence Attached

- [YOLO training results](runs/detect/bender/train/results.csv)
- [Best trained model](runs/detect/bender/train/weights/best.pt)
- [Ground-truth annotations](Dataset/bender.csv)
- [Dataset split](visualizations/data_splits.json)
- [Extracted sequence features](Feature%20Extraction/sequence_features_dataset.csv)

## Caption

Computer-vision pipeline for detecting Bender-Gestalt figures and identifying structural drawing differences using YOLOv8 and template-based Gestalt feature analysis.