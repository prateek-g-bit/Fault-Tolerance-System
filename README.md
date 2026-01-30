# Fault-Tolerant Soil Moisture Estimation

This repository implements a fault-tolerant sensor framework using real-world
soil moisture data from the USDA CAF sensor network.

## Key Features
- Spatial-consensus baseline model
- Synthetic fault injection (bias, extensible)
- Residual-based fault detection
- Conditional fault compensation
- Quantitative fault tolerance evaluation

## Dataset
Raw data is available from:
https://agdatacommons.nal.usda.gov/

Due to size constraints, raw sensor data is not included in this repository.
All experiments were conducted using Kaggle.

## Repository Structure
- `notebooks/` – Main Kaggle notebook
- `baseline/` – Detection thresholds
- `experiments/` – Fault experiment metrics

## Results
For a bias fault of magnitude 0.12 on sensor CAF003:
- RMSE (faulty vs baseline): 0.103
- RMSE (compensated vs baseline): 0.0
- Full recovery achieved on detected samples

## Reproducibility
Run the notebook end-to-end on Kaggle using the provided dataset.
