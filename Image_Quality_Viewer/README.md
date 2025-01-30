Image Quality Viewer 🩺🖼️
---
#### Overview

The **Image Quality Viewer** is a powerful desktop tool designed for analyzing and improving the quality of medical and scientific images. It provides a range of features that allow users to enhance images, analyze noise, and measure image quality. This tool is perfect for researchers, doctors, and anyone who works with images and needs to ensure their quality is as high as possible.

With an easy-to-use interface, users can load, process, and compare images side by side. The application includes advanced features like **contrast improvement**, **noise addition**, and **image filtering**, along with important quality measurements such as **Signal-to-Noise Ratio (SNR)** and **Contrast-to-Noise Ratio (CNR)**. These measurements help assess how clear and useful the images are, which is especially important in medical imaging for accurate diagnoses.

---

## Features

### Image Loading and Display
- **Support for common image formats**: PNG, JPG, BMP
- **Multiple view panels**:  
  - Input image  
  - Output 1 (processed image)
  - Output 2 (secondary processed image)
- **Synchronized display** of original and processed images

### Image Enhancement
- **Histogram Equalization**: Improve contrast by spreading out the most frequent intensity values.
- **CLAHE (Contrast Limited Adaptive Histogram Equalization)**: Adaptive method for enhancing local contrast.
- **Gamma Correction**: Adjust image brightness for better visibility.
- **Brightness and Contrast Adjustment**: Manual adjustments to image brightness and contrast.

### Zoom and Interpolation
- **Multiple zoom levels**:  
  - 0.25x to 5x zoom
- **Various interpolation methods**:  
  - Nearest-Neighbor  
  - Linear  
  - Bilinear  
  - Cubic

### Noise Generation
- **Gaussian Noise**: Add random noise from a Gaussian distribution.
- **Salt and Pepper Noise**: Add random white and black pixels to the image.
- **Speckle Noise**: Introduce noise with varying intensity across pixels.

### Filtering Options
- **Gaussian Filter**: Smoothing filter for noise reduction.
- **Bilateral Filter**: Edge-preserving smoothing filter.
- **Non-Local Means Denoising**: Denoising method that uses a patch-based approach.
- **Low-Pass Filter**: Remove high-frequency noise.
- **High-Pass Filter**: Highlight edges and fine details.

### Analysis Tools
- **Real-time Histogram Visualization**: Dynamic histogram of the image to analyze pixel distribution.
- **SNR (Signal-to-Noise Ratio) Calculation**: Measure the ratio of useful signal to noise.
- **CNR (Contrast-to-Noise Ratio) Calculation**: Evaluate the contrast to noise ratio for image quality assessment.

## Required Libraries

To run the application, install the following libraries:

```bash
pip install PyQt5
pip install opencv-python
pip install numpy
pip install matplotlib
 ```
## Usage

### Run the Application:
To run the application, use the following command:

```bash
python ImageQ.py
```


