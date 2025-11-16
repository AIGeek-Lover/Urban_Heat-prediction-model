# 🌆 Urban Heat Index Prediction: Comparing Landsat and Sentinel-2 Satellite Data

This repository contains three Jupyter Notebooks designed to extract satellite imagery from **Landsat** and **Sentinel-2**, and use them to **predict Urban Heat Index (UHI)** in **New York City**. A machine learning model was trained using extracted indices from both satellites to estimate UHI values, with a comparative evaluation between the two sources.

---

## 📜 About This Project

This project was part of my **first solo data science competition**, organized by **Ernst & Young (EY)**. The goal was to predict urban heat levels using satellite data. I successfully met the competition criteria by achieving an **R² score above 0.80**.

This experience taught me how data science can contribute meaningfully to **sustainability challenges** like urban heat mitigation—an area I am deeply passionate about.

---

## 📁 Notebooks Overview

1. **landsat_extract.ipynb**  
   Extracts relevant bands from **Landsat imagery**, processes them, and computes indices (NDVI, NDBI, NDWI) used for prediction.

2. **sentinel_extract.ipynb**  
   Performs a similar extraction and preprocessing pipeline for **Sentinel-2 imagery**, including band selection and index computation.

3. **predict_uhi.ipynb**  
   Trains and evaluates a machine learning model using an **Extra Trees Regressor**. The model stacks features from both Landsat and Sentinel imagery to predict UHI values.

---

## ⚙️ Key Parameters and Preprocessing Steps

- ✅ **Cloud Cover**: Only images with **< 90% cloud cover** were selected  
- 📏 **Resolution**: All imagery was resampled to **50 meters**  
- 🌿 **Indices Computed**:  
  - NDVI (Normalized Difference Vegetation Index)  
  - NDBI (Normalized Difference Built-up Index)  
  - NDWI (Normalized Difference Water Index)  
- 🗺️ **Geographical Region**: New York City  
- 📆 **Time Frame**: Imagery from **2021**  
- ☁️ **Cloud Removal**: Median compositing was used to reduce cloud interference

---

## 📈 Model and Results

- A **stacked ensemble** model was built using an **Extra Trees Regressor**.
- A comparison was done between Sentinel and Landsat data:  
  - **Sentinel-2** achieved an **R² score of 0.89**  
  - **Landsat** achieved an **R² score of 0.86**  
- The ensemble model performed well on the test set but showed reduced accuracy on unseen inference data, indicating **overfitting**.

---

## 🛠️ How to Run These Notebooks

You can run the notebooks **locally** or on the cloud using **Google Colab**.

### Local Setup

1. Install Jupyter Notebook if you don’t have it yet in the terminal and type jupyter notebook:  
   ```bash
   pip install notebook
   
2. Install the relevant libraries in Jupyter environment 
   pip install numpy xarray matplotlib rioxarray rasterio stackstac pystac-client planetary-computer odc-stac

Or if you would like , feel free to clone the repository

### Clone the Repository

```bash
git clone -v https://github.com/AIGeek-Lover/Urban-Heat-Index-Prediction.git
cd Urban-Heat-Index-Prediction

   
