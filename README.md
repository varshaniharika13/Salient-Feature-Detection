# Salient Feature Detection for Efficient Object Recognition

## Team Members
- Pearl Miglani – 011855836  
- Varsha Niharika Mallampati – 011860708

## Abstract
Salient feature detection identifies the regions in an image that stand out and naturally draw human attention. By integrating this with object detection pipelines, the system focuses only on salient regions, improving both speed and efficiency. This project evaluates different saliency detection techniques using the MIT300 dataset, comparing performance based on accuracy, Intersection over Union (IoU), and processing time.

## Objective
- Improve object detection efficiency by using saliency-based region filtering.
- Evaluate keypoint detection methods (SIFT, ORB) for saliency map generation.
- Integrate saliency maps with an object detection model (YOLOv5).

## Key Technologies
- Python 3.x
- OpenCV (feature detection and saliency modules)
- NumPy, Matplotlib
- YOLOv5 object detection framework
- Google Colab for prototyping and experimentation
- MIT300 Dataset (benchmark eye-tracking data)
- `.npy` files for storing binary saliency masks and ground truth fixation data

## Methods

### Feature Extraction
- **SIFT:** 78% alignment with human fixation points.
- **ORB:** 75% alignment but faster, suitable for real-time applications.

### Saliency Map Construction
- Saliency maps generated from keypoints, contrast, edges, and texture.
- Compared with human fixation points from MIT300 dataset.

### Object Detection Integration
- YOLOv5 processes only salient regions.
- Reduces input size and processing time significantly.

## Key Insights
- Using ORB over SIFT offers a practical speed-accuracy trade-off for real-time applications.
- Saliency maps successfully capture ~82% of human fixation regions, indicating strong alignment with visual attention.
- Filtering object detection to salient regions reduced processing time by ~40% and memory consumption by ~35%, showing improved computational efficiency.
- Intersection over Union (IoU) metric averaging 0.60 confirms moderate to good overlap of predicted salient regions with ground truth.

