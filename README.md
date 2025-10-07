# Ionosphere AI Prediction System

## Project Overview
This project predicts ionospheric behavior (Total Electron Content, TEC) using deep learning (LSTM) based on:
- GAGAN grid TEC data
- Polar Cap Index (PCI)
- Geomagnetic indices (Kp, Dst)
- Solar activity (F10.7 flux)
- Time and location features

The model aims to improve satellite navigation, communication, and early detection of ionospheric disturbances.

## Folder Structure
- `data/` : Raw & processed datasets
- `notebooks/` : EDA, preprocessing, and training exploration
- `src/` : Core Python scripts (data loading, preprocessing, modeling, prediction)
- `app/` : Deployment apps (Streamlit / Flask)
- `utils/` : Plotting and helper functions
- `models/` : Saved trained LSTM models

## Setup
1. Install dependencies:
```bash
pip install -r requirements.txt
