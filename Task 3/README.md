
# Forest Cover Type Classification

Predict forest cover types using environmental and cartographic features from the **Covertype dataset (UCI)**.

---

## Dataset

- **Source:** [UCI Covertype dataset](https://archive.ics.uci.edu/ml/datasets/covertype)  
- **Features:** 54 features + soil type   
- **Target:** `Cover_Type` (classes 1–7)

---

## Preprocessing

- Converted one-hot soil type columns into a single categorical column `Soil_Type`.  
- Dropped the original 40 soil type columns.  
- Split data: 70% training, 30% testing.

---

## Models & Performance

| Model           | Accuracy | ROC AUC |
|-----------------|---------|---------|
| Decision Tree   | 93.28%  | 0.935   |
| Random Forest   | 95.65%  | 0.997   |

- **Hyperparameter tuning:**  
  - Decision Tree (entropy, max_depth=220) → 93.79%  
  - Random Forest (200 trees, entropy) → 95.97%

