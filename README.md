# IoT Network Traffic Classification

A machine learning project to classify IoT network traffic into attack types using the IoT dataset with flow rates.

## Dataset
- **238,687** network flow records
- **34 attack classes** (DDoS, DoS, Mirai, Recon, etc.) + Benign traffic
- **49 features** including flow duration, packet rates, TCP flags, protocol types

## Pipeline
1. **EDA** — class distribution plot, basic statistics
2. **Feature Engineering** — `rate_ratio`, `total_flags`, `bytes_per_pkt`
3. **Feature Scaling** — MinMaxScaler (0–1 range)
4. **Train/Test Split** — 80/20 stratified
5. **Model** — Random Forest (100 trees)

## Results
Run `my.ipynb` to reproduce results including accuracy, precision, recall, and F1-score per class.

## Requirements
```
pip install -r requirements.txt
```

## Usage
```
jupyter notebook my.ipynb
```
