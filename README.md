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


---

Money Sharma
