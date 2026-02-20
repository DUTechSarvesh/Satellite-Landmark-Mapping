# 📡 NOAA Satellite Image Acquisition & Enhancement System  

## 🚀 Project Overview  

This project presents a complete end-to-end system for:

- 📡 Receiving NOAA weather satellite signals  
- 🔊 Decoding APT (Automatic Picture Transmission) signals  
- 🖼 Enhancing satellite imagery  
- 🧠 Reconstructing corrupted image segments  
- 🌍 Performing landmark segmentation using K-Means clustering  

The system captures real-time Earth imagery from **NOAA-15, NOAA-18, and NOAA-19** satellites using WebSDR and processes the decoded images using advanced image processing techniques in MATLAB.

---

## 🎯 Objectives  

- Receive and decode analog APT signals from NOAA satellites  
- Enhance noisy satellite images using filtering techniques  
- Reconstruct corrupted line segments using Hough Transform  
- Perform landmark mapping using K-Means clustering  
- Build a cost-effective, hardware-free satellite imaging workflow  

---

## 🛰️ Satellites Used  

| Satellite | Frequency (MHz) | Orbit Type | Altitude |
|------------|----------------|------------|----------|
| NOAA-15 | 137.620 | Sun-synchronous | ~870 km |
| NOAA-18 | 137.9125 | Sun-synchronous | ~854 km |
| NOAA-19 | 137.100 | Sun-synchronous | ~870 km |

These satellites broadcast real-time weather imagery via APT signals in the 137 MHz band.

---

## 🏗 System Workflow  

### 1️⃣ Satellite Tracking  
- Satellite passes predicted using online tracking tools  
- Recording scheduled during overhead passes  

### 2️⃣ Signal Reception  
- WebSDR used for tuning into 137 MHz frequency band  
- Audio recorded in WAV format  

### 3️⃣ Signal Decoding  
- APT signals decoded using SatDump  
- Generated grayscale satellite images  

### 4️⃣ Image Enhancement  

#### 🔹 Gaussian Filtering  
- Reduces high-frequency Gaussian noise  
- Smooths image  

#### 🔹 Median Filtering  
- Removes salt-and-pepper noise  
- Preserves edges  

---

## 🧱 Image Reconstruction (Hough Transform)

The Hough Transform is used to:

- Detect corrupted horizontal noise lines  
- Identify strong line structures  
- Reconstruct broken segments  
- Improve image continuity  

Techniques used:
- Canny Edge Detection  
- Hough Transform  
- Hough Peaks  
- Line Extraction  
- Morphological Operations  

---

## 🌍 Landmark Mapping Using K-Means Clustering  

K-Means clustering (k = 4) is applied to segment the satellite image into:

- 🌊 Ocean  
- 🟫 Land  
- ☁ Clouds  
- 🌿 Vegetation  

False coloring is applied for better visualization and interpretation.

---

## 🛠 Technologies & Tools Used  

- WebSDR (Signal Reception)  
- SatDump (APT Decoding)  
- MATLAB (Image Processing & Machine Learning)  
- Canny Edge Detection  
- Hough Transform  
- K-Means Clustering  

---

## 📊 Results  

✔ Successful real-time satellite image acquisition  
✔ Effective noise reduction using combined filters  
✔ Detection and reconstruction of corrupted lines  
✔ Clear segmentation of land, water, vegetation, and clouds  
✔ Hardware-free SDR-based implementation  

---

## 💡 Innovations & Uniqueness  

- ✅ Hardware-free satellite reception using WebSDR  
- ✅ Advanced post-processing beyond basic APT decoding  
- ✅ Integration of signal processing + image processing + ML  
- ✅ Cost-effective Earth observation system  

---

## 🔮 Future Scope  

- Automation of satellite tracking & decoding  
- Machine Learning-based weather classification  
- HRPT high-resolution reception  
- Georeferencing and map overlay  
- Real-time dashboard visualization  

---

## 📂 Project Structure  

```
NOAA-Satellite-Image-Enhancement/
│
├── raw_audio/
├── decoded_images/
├── filtered_images/
├── hough_reconstruction/
├── kmeans_segmentation/
├── matlab_code/
└── README.md
```

---

## 👨‍💻 Author  

**Sarvesh Kumar**  
B.Tech – Electronics & Communication Engineering  
Faculty of Technology, University of Delhi  

---

## ⭐ If You Found This Project Interesting  

Give it a ⭐ on GitHub and feel free to contribute!
