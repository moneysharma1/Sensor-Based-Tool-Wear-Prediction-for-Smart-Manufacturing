# CNC Tool Wear Prediction

## ASSESSMENT

Logistic Regression beat Random Forest.

| Model | Accuracy |
|------|----------|
| Logistic Regression | 93.3% |
| Random Forest | 86.7% |

This dataset favored a simpler model.

Most useful signals:

- time  
- run  
- spindle vibration

---

## USE

Predict whether a tool is likely healthy or worn from machine data.

Can support:

- earlier checks  
- cleaner replacement decisions  
- lower defect risk

Not a timing model. Condition model.

---

## APPROACH

Built a binary classifier using CNC process + sensor data.

Target:

- 0 = Healthy  
- 1 = Worn

Threshold used:

- VB >= 0.30

Models tested:

- Logistic Regression  
- Random Forest

---

## RESULTS

### Confusion Matrix
Low misclassification on unseen data suggests tool state was learnable from available signals.

<img width="498" height="453" alt="image" src="https://github.com/user-attachments/assets/b4e8504a-aef5-46e1-a0ba-8157a9ae149d" />

### Feature Importance
Usage and vibration variables carried stronger signal than several static settings.

<img width="603" height="433" alt="image" src="https://github.com/user-attachments/assets/0649783b-fb17-44b0-9147-59c65394b81a" />


## Project Scope

This project is a condition classification model for CNC tool wear.

It uses CNC sensor and process data to classify tool condition as `healthy` or `worn` based on a defined wear threshold.

The target label was derived from `VB` because `VB` directly represents measured tool wear. Other variables such as vibration, acoustic emission, spindle current, feed, depth of cut, run, and time were used as input features because they describe machine behavior and process conditions related to wear.

The project focuses on:
- converting measured tool wear into classification labels
- comparing Logistic Regression and Random Forest
- evaluating model performance using classification metrics
- interpreting feature influence on the prediction

This is not a Remaining Useful Life model.  
It does not predict failure time or remaining operating time.

## Next Development Direction

The next development direction is Remaining Useful Life estimation.

This reframes the project from condition classification to time-to-failure prediction. Instead of classifying the current tool state as `healthy` or `worn`, the goal is to estimate the remaining operating time before the tool reaches a critical wear condition.

A further extension is failure-mode classification, where the model identifies the failure type or affected component if suitable labeled data is available.

Money Sharma
