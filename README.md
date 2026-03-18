
# Image Contrast Enhancement in HSV Color Space

This repository contains a MATLAB-based project completed as part of the **MathWorks: Introduction to Image Processing** course on Coursera. The project focuses on enhancing the visibility of night-time photography by manipulating the "Value" (Brightness) channel in the HSV color space using four distinct contrast adjustment techniques.

# 📌 Project Overview
The goal of this project was to take a low-light RGB image ("boston night.jpg") and improve its contrast and brightness without distorting the original color balance. This was achieved by:

1. Converting the image from **RGB** to **HSV** (Hue, Saturation, Value).

2. Applying mathematical and algorithmic adjustments to the **Value (V)** channel.

3. Reconstructing the color image back to RGB.

# 🛠️ Image Processing Techniques Used
I implemented and compared four different methods for contrast adjustment:

- **Gamma Correction (γ=1/2):** A non-linear operation used to decode and encode luminance. Setting γ<1 effectively brightens the shadows and mid-tones.

- **Intensity Scaling (imadjust):** Maps the intensity values to a new range, saturating the bottom and top 1% of all pixel values by default to increase global contrast.

- **Histogram Equalization (histeq):** Adjusts the intensity values so that the histogram of the output image approximately matches a flat (uniform) distribution.

- **Contrast-Limited Adaptive Histogram Equalization (adapthisteq):** Unlike global equalization, this operates on small regions (tiles) of the image, enhancing local contrast while preventing over-amplification of noise.

# 💻 MATLAB Implementation
The core workflow follows these steps:

1. **Color Space Conversion:** rgb2hsv()

2. **Channel Processing:** Manipulating the third dimension of the HSV matrix.

3. **Re-conversion: hsv2rgb()**

4. **Data Type Correction:** Converting from double back to uint8 for standard image viewing.

## Visualizing the Results

The final output is displayed as a montage to compare the efficacy of each method:

Matlab
montage({imgGamma, imgAdjust, imgEq, imgAdapt})

# 🚀 How to Run
1. Ensure you have **MATLAB** installed.

2. Clone this repository.

3. Place boston night.jpg in the root folder.

4. Run the main script to generate the contrast-adjusted montages.

## About the Author

**Dr. Shahadat Hussain**

Researcher in 3D Printing & Materials Science. I use Image Processing to analyze material structures and 3D printing failure modes.

🌐 [www.shahadathussain.com](https://www.shahadathussain.com) | ✍️ [Substack](https://drshahadathussain.substack.com)
