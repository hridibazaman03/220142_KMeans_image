# 220142_KMeans_image

# 220142_KMeans_Image

## Project Overview
This project implements the K-Means Clustering algorithm for Image Color Quantization using Python and Scikit-Learn.

The model is trained on a standard image by clustering RGB pixel values into a smaller number of representative colors. The trained model is then applied to a custom image to perform real-world color compression.

---

## Dataset

### Standard Dataset
- File: `dataset/Standard_image.jpg`
- Purpose: Training the K-Means model.

### Custom Dataset
- File: `dataset/Custom_photo.jpg`
- Purpose: Testing the trained model on a real-world image.

---

## Data Preprocessing

- Image loaded using PIL.
- Image resized to 300 × 300 pixels.
- RGB pixels extracted and reshaped into a 2D dataset.
- StandardScaler applied to normalize pixel values before clustering.

---

## Elbow Method

The optimal number of clusters (K) was determined using the Elbow Method by calculating the Within Cluster Sum of Squares (WCSS) for different K values.

### Elbow Curve

![Elbow Curve](images/elbow_curve.png)

---

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

---

## Cluster Visualization

The clusters were visualized using PCA to reduce the RGB feature space to two dimensions.

### Cluster Scatter Plot

![Cluster Plot](images/cluster_scatter.png)

---

## Image Compression Results

### Standard Image

| Original | Compressed |
|-----------|-----------|
| Add Screenshot Here | Add Screenshot Here |

### Custom Image

| Original | Compressed |
|-----------|-----------|
| Add Screenshot Here | Add Screenshot Here |

---

## Custom Prediction Output

Example output:

| Pixel | R | G | B | Cluster_ID |
|---------|---------|---------|---------|---------|
| Pixel_1 | 120 | 135 | 140 | 2 |
| Pixel_2 | 55 | 70 | 85 | 5 |
| Pixel_3 | 210 | 205 | 195 | 1 |
| ... | ... | ... | ... | ... |

---

## Cluster Interpretation

The K-Means algorithm identified 8 dominant color groups in the training image. Each cluster centroid represents a representative RGB color that summarizes a large group of visually similar pixels.

During image reconstruction, every pixel is replaced by its nearest centroid color, reducing the total number of colors while preserving the overall appearance of the image. This enables image compression while maintaining most visual details.

---

## Repository Structure

```
220142_KMeans_image/
│
├── dataset/
│   ├── Standard_image.jpg
│   └── Custom_photo.jpg
│
├── model/
│   ├── kmeans_model.pkl
│   └── scaler.pkl
│
├── 220142_KMeans_Image.ipynb
│
└── README.md
```

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-Learn
- PIL (Python Imaging Library)

---

## Author

Student ID: 220142
