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

  
## File Structure
IonosphereAI/
│
├── data/
│   ├── raw/                   # Raw data from GAGAN, PCI, Kp, Dst, F10.7
│   │   ├── tec_data.csv
│   │   ├── pci_data.csv
│   │   └── solar_geomag.csv
│   ├── processed/             # Cleaned & merged datasets ready for ML
│   │   └── merged_data.csv
│   └── external/              # Optional: any third-party datasets
│
├── notebooks/
│   ├── 01_data_exploration.ipynb   # Exploratory Data Analysis (EDA)
│   ├── 02_preprocessing.ipynb      # Data cleaning, normalization, sequence building
│   └── 03_model_training.ipynb     # LSTM model training and evaluation
│
├── src/
│   ├── __init__.py
│   ├── data_loader.py          # Functions to load & merge datasets
│   ├── preprocessing.py        # Functions for cleaning, normalization, sequence creation
│   ├── model.py                # LSTM model architecture & training function
│   ├── train.py                # Script to train the model
│   ├── evaluate.py             # Script to evaluate & visualize model predictions
│   └── predict.py              # Script/API to make predictions on new data
│
├── app/
│   ├── streamlit_app.py        # Streamlit dashboard for visualization
│   └── flask_app.py            # Flask API (optional)
│
├── utils/
│   ├── visualization.py        # Functions for plotting TEC, heatmaps, correlations
│   └── helpers.py              # Misc helper functions
│
├── models/
│   └── lstm_model.h5           # Saved trained LSTM model
│
├── requirements.txt            # All Python dependencies (tensorflow, pandas, numpy, etc.)
├── config.yaml                 # Config file for paths, hyperparameters
├── README.md                   # Project overview & instructions
└── .gitignore                  # Ignore unnecessary files (datasets, model weights)


## Setup
1. Install dependencies:
```bash
pip install -r requirements.txt

