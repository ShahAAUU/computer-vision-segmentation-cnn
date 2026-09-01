# Computer Vision: Image Segmentation & CNN Classification

Coursework project (COM675) covering two computer vision tasks: foreground segmentation on custom images and CNN-based image classification with a customised dataset.

## Overview

- **Type:** Image segmentation + image classification
- **Techniques used:** HSV thresholding, GrabCut/watershed segmentation, Convolutional Neural Networks (CNN)
- **Language/Tools:** Python, OpenCV, TensorFlow, Keras
- **Context:** COM675 Computer Vision coursework, Ulster University

## Part A — Image Segmentation

Segmented the foreground from a self-collected set of original images (captured by phone/camera, not sourced online) using two different approaches:

1. **HSV thresholding / edge-based segmentation**
2. **An alternative method** (GrabCut or watershed)

Results from both methods are compared to evaluate which performed better on the collected images, and why.

## Part B — Image Classification (CNN)

Built and compared two CNN models for image classification:

- **Baseline CNN:** `Conv → Pool → Conv → Pool → Flatten → Dense → Dropout → Softmax`
- **Modified CNN:** baseline architecture extended with at least three changes (e.g. additional layers, batch normalization, data augmentation) aimed at improving performance

### Dataset

- A **three-class dataset** sampled from the provided coursework dataset
- A **customised dataset**: the three-class dataset merged with self-collected images (10+ per class, captured independently)
- Both datasets split into training/validation/test sets

### Evaluation

Both models were evaluated and compared on:
- Accuracy
- Confusion matrix
- Precision and recall
- Training/validation loss curves

## How to Run

```bash
# clone the repo
git clone https://github.com/ShahAAUU/computer-vision-segmentation-cnn.git
cd computer-vision-segmentation-cnn

# install dependencies
pip install opencv-python tensorflow keras numpy matplotlib

# open the notebooks
jupyter notebook part_a_segmentation.ipynb
jupyter notebook part_b_classification.ipynb
```

## Project Structure

```
├── part_a_segmentation.ipynb
├── part_a_segmentation.html
├── part_b_classification.ipynb
├── part_b_classification.html
└── images/          # self-collected images used for segmentation/classification
```

## Notes

Both classification models were trained and evaluated on the same three-class and customised datasets to directly compare the effect of the architectural changes made in the modified CNN.
