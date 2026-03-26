# LSTM Air Quality Forecasting

A tutorial on using Long Short-Term Memory (LSTM) neural networks to forecast hourly CO concentration from the UCI Air Quality dataset.

## What this repo contains

| File | Description |
|------|-------------|
| `lstm_air_quality_tutorial.ipynb` | Complete Jupyter notebook — run top to bottom |
| `tutorial_lstm_air_quality.pdf` | Written tutorial (the submission document) |
| `AirQuality.csv` | Source data (download from Kaggle — see below) |

## Getting the data

Download `AirQuality.csv` from:  
https://www.kaggle.com/datasets/fedesoriano/air-quality-data-set

Place it in the same folder as the notebook before running.

## Requirements

```
pip install tensorflow scikit-learn matplotlib pandas numpy
```

Tested on Python 3.10, TensorFlow 2.15.

## Running the notebook

```bash
jupyter notebook lstm_air_quality_tutorial.ipynb
```

Run all cells in order. Training takes around 3–5 minutes on a standard CPU.

## What the tutorial covers

1. Why LSTM suits time-series pollution data
2. Loading and cleaning the UCI Air Quality dataset
3. Building a sliding-window supervised problem
4. Training a two-layer stacked LSTM with early stopping
5. Comparing predictions against a naive persistence baseline
6. How to adapt the code to other pollutants or datasets

## Results summary

| Model | MAE (mg/m³) | RMSE (mg/m³) |
|-------|-------------|--------------|
| LSTM | ~0.46 | ~0.68 |
| Naive baseline | ~0.51 | ~0.80 |

## Accessibility

- All plots use colour-blind-friendly palettes (blue/orange)
- All figures include descriptive alt-text in the PDF
- The notebook is structured with clear markdown headings for screen readers

## References

- Hochreiter & Schmidhuber (1997). Long Short-Term Memory. *Neural Computation*.
- De Vito et al. (2008). On field calibration of an electronic nose. *Sensors and Actuators B*.
- Chollet, F. (2021). *Deep Learning with Python*, 2nd ed. Manning.

## Licence

This tutorial is released under the [MIT Licence](LICENSE). You are free to use, adapt, and share it with attribution.
