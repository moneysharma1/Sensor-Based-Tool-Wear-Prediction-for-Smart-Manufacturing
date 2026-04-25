# Sensor-Based Tool Wear Prediction for Smart Manufacturing
Machine learning project for predicting CNC tool wear and maintenance risk using industrial sensor data.


## Project Overview

Built a machine learning project to predict whether a CNC cutting tool is healthy or worn using sensor and process data.

The goal is predictive maintenance: detect wear early and reduce downtime, waste, and unexpected tool failure.

## Dataset Features

Variables used:

* case
* run
* time
* DOC
* feed
* material
* smcAC
* smcDC
* vib_table
* vib_spindle
* AE_table
* AE_spindle

Target variable:

* wear_flag
  0 = healthy
  1 = worn

Created using tool wear value `VB >= 0.30`.

## Models Tested

* Logistic Regression
* Random Forest Classifier

## Results

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 93.3%    |
| Random Forest       | 86.7%    |

## Key Findings

* Simpler linear model performed better than Random Forest on current data.
* Sensor values contain strong predictive signal.
* Run, time, and spindle vibration showed high importance.

## Project Structure

```text
notebooks/
models/
README.md
requirements.txt
```

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

Open the notebook and run cells in order.

## Business Value

This type of system can help factories:

* Schedule maintenance earlier
* reduce machine stoppage
* lower scrap cost
* improve production planning

## Author

Money Sharma
Applied Artificial Intelligence
TH Rosenheim

