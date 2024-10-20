# TP_Image_Classification

This repository contains a lab focused on image classification using a Bag-of-Words (BoW) approach and Histograms of Oriented Gradients (HOG) descriptors, combined with K-means clustering. The lab provides practical insights into applying computer vision techniques for image classification tasks.

## Summary

The lab covers the following topics:

1. **Bag-of-Words Classification Pipeline:**
   - The BoW model converts raw image data into structured patterns by extracting HOG features and clustering them with K-means. Images are then represented by histograms that map their features to a predefined set of visual words.
   - A nearest neighbor classifier is used to label new images based on the BoW histograms.

2. **Feature Extraction with HOG:**
   - The HOG descriptor captures edge patterns in images by computing gradient magnitudes and orientations. These descriptors are used to represent local shape and texture.
   - Parameters such as cell size, block size, and the number of bins are chosen to balance detail capture and computational efficiency.

3. **Visual Vocabulary Construction with K-means Clustering:**
   - The K-means algorithm clusters HOG descriptors into visual words, forming a dictionary that represents images compactly. Images are then classified based on the distribution of these visual words.

4. **Experimentation:**
   - Multiple tests were conducted with varying numbers of clusters (K values) and distance norms (L1 and L2) to assess classification accuracy.
   - Lower cluster counts (e.g., K=2) yielded higher accuracy, while higher values resulted in significant overlap, leading to poor classification.

## Requirements

To run the notebook, you will need the following Python libraries:
- NumPy
- OpenCV (cv2)
- Matplotlib
- Scipy
- Sklearn

You can install these dependencies via pip if needed:
```bash
pip install numpy opencv-python-headless matplotlib scipy scikit-learn
