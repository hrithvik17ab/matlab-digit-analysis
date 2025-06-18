# MATLAB Handwritten Digit Feature Analysis

### Author: Hrithvik Ranka

---

## Project Overview

This MATLAB project demonstrates a complete computer vision pipeline for feature extraction and analysis. The script uses a built-in dataset of handwritten digits, extracts key geometric and topological features from each image, and analyzes the consistency of those features across different digit classes. This project showcases the ability to programmatically analyze and draw conclusions from a set of images without any external dependencies.

---

## How It Works

The script performs the following steps automatically:

1.  **Load Data**: Loads the MNIST handwritten digits dataset, which is built directly into MATLAB. This avoids any potential download errors.
2.  **Image Processing**: Each grayscale image is binarized to create a clean, black-and-white silhouette of the digit.
3.  **Feature Extraction**: The powerful `regionprops` function is used to automatically calculate key features for each digit's shape, including:
    * **Area**: The number of pixels making up the digit.
    * **Eccentricity**: A measure of how elongated the shape is.
    * **Euler Number**: A topological feature that measures connectivity (e.g., a '5' is a single solid object, while an '8' contains two holes).
4.  **Analysis & Visualization**: The script groups the results by digit label (0-9) and generates a box plot to visualize the consistency of the extracted features.

---

## Key Result

The final plot demonstrates a key finding: the **Euler Number** is a highly consistent and effective feature for distinguishing certain digits. As shown below, the digit '8' consistently has an Euler Number of -1 (indicating two holes), while digits like '0', '4', and '6' have a value of 0 (one hole). This proves the success of the feature extraction algorithm.

---

## How to Run the Code

1.  Ensure you have MATLAB with the Deep Learning Toolbox and Image Processing Toolbox installed.
2.  Open the `digit_feature_analysis.m` file in MATLAB.
3.  Click the "Run" button. The script will execute and generate the final analysis plot.

## Technologies Used

* MATLAB
* Image Processing Toolbox
* Deep Learning Toolbox (for the built-in dataset)
