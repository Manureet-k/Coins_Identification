# Coins_Identification

This project aims to automatically identify and classify coins of different denominations using image processing techniques. The system takes an image of coins as input and applies segmentation, morphological operations, and feature extraction to detect and recognize the coin values.
It is useful for applications like automated coin sorters, vending machines, or financial digitization where physical currency needs to be recognized efficiently.


## Tech Stack
Python – Core programming language
OpenCV – For image processing and computer vision tasks
NumPy – Numerical computations and matrix operations
Matplotlib – Visualizing the processing steps (optional)
Jupyter Notebook – For step-by-step development and testing


## Steps Performed for Coin Detection

1. Image Preprocessing
    a. Load the input coin image using OpenCV.
    b. Convert the image to grayscale for easier processing.
    c. Apply Gaussian Blur to reduce noise and smooth the image.

2. Thresholding: Use Otsu’s Thresholding or Adaptive Thresholding to convert the grayscale image to a binary image (black & white). This helps in distinguishing coin regions from the background.

3. Morphological Processing
    a. Use Erosion and Opening operations to:
    b. Remove small noise.
    c. Separate coins that are touching slightly.
    d. Use Dilation to define the background more clearly if needed.

4. Contour Detection
    a. Find contours from the morphologically cleaned binary image.
    b. Draw contours on the original image to visualize coin boundaries.
    c. Count the number of coins by counting the number of detected contours.

5. Segmentation of Individual Coins: For each detected contour,
    a. Calculate bounding boxes.
    b. Extract and display each individual coin region.

6. Advanced Coin Separation (Overlapping Coins): For overlapping coins,
    a. Apply Distance Transform and Watershed Algorithm.
    b. Use markers to differentiate foreground (coins) and background.
    c. Detect and draw circles or contours around coins even if they overlap.



