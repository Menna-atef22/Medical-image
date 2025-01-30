# Image Quality Viewer 🩺  

The Image Quality Viewer is a powerful desktop application designed for medical and scientific image analysis. It provides a comprehensive suite of tools for image enhancement, noise analysis, and quality assessment, making it ideal for researchers, medical professionals, and image processing specialists.  

This application enables users to load medical or scientific images and apply various processing techniques in real-time. With its intuitive interface featuring three display panels (Input, Output 1, Output 2), users can easily compare different processing results side by side.  

The tool supports advanced operations such as contrast enhancement, noise simulation, filtering, and quantitative measurements, including **SNR (Signal-to-Noise Ratio)** and **CNR (Contrast-to-Noise Ratio)** calculations, essential for medical image quality assessment.  

---

## Features ✨  

### Image Loading and Display  
- **Support for common image formats**: PNG, JPG, BMP.  
- **Multiple view panels**: Input, Output 1, Output 2.  
- **Synchronized display** of original and processed images.  

### Image Enhancement  
- Histogram Equalization.  
- CLAHE (Contrast Limited Adaptive Histogram Equalization).  
- Gamma Correction.  
- Brightness and Contrast adjustment.  

### Zoom and Interpolation  
- Multiple zoom levels (0.25x to 5x).  
- Various interpolation methods:  
  - Nearest-Neighbor.  
  - Linear.  
  - Bilinear.  
  - Cubic.  

### Noise Generation  
- Gaussian noise.  
- Salt and Pepper noise.  
- Speckle noise.  

### Filtering Options  
- Gaussian filter.  
- Bilateral filter.  
- Non-Local Means denoising.  
- Low-Pass filter.  
- High-Pass filter.  

### Analysis Tools  
- **Real-time histogram visualization**.  
- **SNR (Signal-to-Noise Ratio) calculation**.  
- **CNR (Contrast-to-Noise Ratio) calculation**.  

---

## Signal-to-Noise Ratio (SNR) 📊  

**SNR (Signal-to-Noise Ratio)** is a key metric for assessing the quality of medical and scientific images. It measures the ratio of the mean signal intensity to the standard deviation of the noise, indicating the clarity of the image relative to noise.  

### SNR Formula  
The application calculates SNR using the formula:  
\[

SNR = mean(signal) / std(noise)

\]  

Where:  
- `mean(signal)` is the average intensity in the selected signal region.  
- `std(noise)` is the standard deviation of pixel intensities in the noise region.  

### How to Calculate SNR in the Application:  
1. Load an image using the **"Load Image"** button.  
2. Select **ROIs (Regions of Interest)** for the signal and noise areas:  
   - Use the cursor to draw rectangles around the regions you want to analyze.  
   - Assign the signal region (e.g., an area containing meaningful data).  
   - Assign the noise region (e.g., a background area).  
3. Click **"Calculate SNR"** in the control panel.  
4. The SNR value will be displayed in the analysis panel or console output.  

**Example**:  
- If the mean signal intensity is `100` and the standard deviation of noise is `10`, the SNR is calculated as:  
  \[
  
  SNR = 100 / 10 =10

  \]  

---

### CNR (Contrast-to-Noise Ratio)

**CNR** (Contrast-to-Noise Ratio) is a metric used to assess the contrast between two regions in an image while considering the level of noise. It is primarily used in medical and scientific image analysis to determine the clarity of details within the image. CNR helps in identifying the ability to distinguish between high-contrast areas and those containing noise.

### CNR Formula  
The application calculates **CNR (Contrast-to-Noise Ratio)** using the formula:  
\[
CNR = \frac{|mean(region1) - mean(region2)|}{std(noise)}
\]

Where:  
- `mean(region1)` is the average intensity in the first selected region (e.g., a region containing an object of interest).  
- `mean(region2)` is the average intensity in the second selected region (e.g., a background or comparison region).  
- `std(noise)` is the standard deviation of pixel intensities in the noise region.  

### How to Calculate CNR in the Application:  
1. Load an image using the **"Load Image"** button.  
2. Select **ROIs (Regions of Interest)** for the two regions of interest and the noise area:  
   - Use the cursor to draw rectangles around the regions you want to analyze.  
   - Assign the first region (e.g., an area containing an object of interest).  
   - Assign the second region (e.g., a background or comparison region).  
   - Assign the noise region (e.g., an area without significant features).  
3. Click **"Calculate CNR"** in the control panel.  
4. The CNR value will be displayed in the analysis panel or console output.  

**Example**:  
- If the mean intensity of region 1 is `120`, the mean intensity of region 2 is `80`, and the standard deviation of noise is `15`, the CNR is calculated as:  
  \[
  CNR = \frac{|120 - 80|}{15} = \frac{40}{15} \approx 2.67
  \]
---
## Screenshots 📸  

### Output 1: Applying Noise | Output 2: Applying Filter  
![Noise and Filter](Image_Quality_Viewer/images/filter & noise.png)  

### Output 1: Contrast Enhancement | Output 2: 3x Zoom  
![Contrast and Zoom](Image_Quality_Viewer/images/contrast & zoom x3.png)  

### Selecting ROIs for CNR Calculation  
![SNR Calculation](Image_Quality_Viewer/images/CNR.png)  

### Selecting ROIs for SNR Calculation  
![SNR Calculation](Image_Quality_Viewer/images/SNR.png)  

### Histogram of Input (#pixels & Intensity)  
![Histogram](Image_Quality_Viewer/images/Histogram.png)  

*(Replace `path/to/your/...` with actual paths to your screenshots in the repository.)*  

---

## Required Libraries 📚  

Install the required libraries using pip:  
```bash
pip install PyQt5
pip install opencv-python
pip install numpy
pip install matplotlib
