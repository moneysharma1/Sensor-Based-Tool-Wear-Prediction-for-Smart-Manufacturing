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

## Current Project Status

This project currently works as a condition classification model.  
It predicts whether a CNC tool is likely healthy or worn based on sensor and process data.

The model does not yet estimate failure time or Remaining Useful Life (RUL). It is focused on classifying the current tool condition.

## Next Development Step

The next practical step is to turn the trained model into a usable prediction service.

Planned work for the next version:

1. Save the trained model using `joblib`.
2. Create a FastAPI endpoint for model prediction.
3. Accept CNC sensor and process values as JSON input.
4. Return a prediction such as `healthy` or `worn`.
5. Add example API requests and responses to the README.
6. Move reusable preprocessing and prediction logic from the notebook into Python scripts.


---

Money Sharma
