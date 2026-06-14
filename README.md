# 220142_KMeans_Image

## Project Overview
This project implements the K-Means Clustering algorithm for Image Color Quantization using Python and Scikit-Learn. The model is trained on a standard image by clustering RGB pixel values into a smaller number of representative colors. The trained model is then applied to a custom image to perform real-world color compression.

## Dataset

### Standard Dataset
- File: `dataset/Standard_image.jpg`
- Purpose: Training the K-Means model.

### Custom Dataset
- File: `dataset/Custom_photo.jpg`
- Purpose: Testing the trained model on a real-world image.

## Data Preprocessing

- Image loaded using PIL.
- Image resized to 300 × 300 pixels.
- RGB pixels extracted and reshaped into a 2D dataset.
- StandardScaler applied to normalize pixel values before clustering.

## Elbow Method

The optimal number of clusters (K) was determined using the Elbow Method by calculating the Within Cluster Sum of Squares (WCSS) for different K values.

### Elbow Curve

![Elbow Curve](https://github.com/hridibazaman03/220142_KMeans_image/blob/a388b8c3a5e1abb7654df37cfd0a87ec5220320e/Screenshots/KMeans%20elbow%20curve.png)

## Model Training

Algorithm:
- K-Means Clustering

Parameters:
- Number of Clusters (K): 8
- Random State: 42
- n_init: 10

Saved Files:
- `model/kmeans_model.pkl`
- `model/scaler.pkl`

## Cluster Visualization

The clusters were visualized using PCA to reduce the RGB feature space to two dimensions.

### Cluster Scatter Plot

![Cluster Plot](https://github.com/hridibazaman03/220142_KMeans_image/blob/a388b8c3a5e1abb7654df37cfd0a87ec5220320e/Screenshots/KMeans%20custom%20scatter%20plot.png)

## Image Compression Results

### Standard Image

![standard](https://github.com/hridibazaman03/220142_KMeans_image/blob/38f991235740c9744b6d62da53252d6428e73770/Screenshots/KMeans%20standard%20image%20compressed.png)

### Custom Image

![standard](https://github.com/hridibazaman03/220142_KMeans_image/blob/38f991235740c9744b6d62da53252d6428e73770/Screenshots/KMeans%20custom%20image%20compressed.png)


## Custom Prediction Output

![standard](https://github.com/hridibazaman03/220142_KMeans_image/blob/38f991235740c9744b6d62da53252d6428e73770/Screenshots/KMeans%20custom%20prediction%20output.png)

## Cluster Interpretation

The K-Means algorithm identified 8 dominant colour groups in the training image. Each cluster centroid represents a representative RGB colour that summarizes a large group of visually similar pixels. During image reconstruction, every pixel is replaced by it's nearest centroid colour, reducing the total number of colours while preserving the overall appearance of the image. This enables image compression while maintaining most visual details.
