# 🎓 GRE Score Prediction using Artificial Neural Network (ANN)

This project uses a deep neural network built with **Keras (TensorFlow backend)** to predict **graduate admissions chances** based on GRE scores and other academic features. The model is trained on the popular Kaggle dataset: [Graduate Admissions](https://www.kaggle.com/datasets/mohansacharya/graduate-admissions).

---

## 📊 Dataset

- **Source:** Kaggle - [Graduate Admissions Dataset](https://www.kaggle.com/datasets/mohansacharya/graduate-admissions)
- **Rows:** 500  
- **Features:** 7 independent variables + 1 target (`Chance of Admit`)
  
### 🧾 Features Used:

| Feature            | Description                                     |
|--------------------|-------------------------------------------------|
| GRE Score          | Graduate Record Exam score (out of 340)        |
| TOEFL Score        | TOEFL exam score (out of 120)                  |
| University Rating  | Rating of the university (1 to 5)              |
| SOP                | Statement of Purpose strength (1 to 5)         |
| LOR                | Letter of Recommendation strength (1 to 5)     |
| CGPA               | Undergraduate GPA (out of 10)                  |
| Research           | Research experience (0 or 1)                   |

---

## 🤖 Model Architecture

A **fully connected feed-forward ANN** using the Keras `Sequential` API:

```python
Input(shape=(7,))
Dense(16, activation='relu')
Dropout(0.2)
Dense(8, activation='relu')
Dense(4, activation='relu')
Dense(2, activation='relu')
Dense(1, activation='linear')
```

### ✅ Optimizer & Loss
- **Optimizer:** AdamW (improved version of Adam)
- **Loss Function:** Mean Squared Error (MSE)
- **Evaluation Metric:** Mean Absolute Error (MAE)

---

## 🛠 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/hendrix0731/GRE-Prediction-ANN.git
   cd GRE-Prediction-ANN
   ```

2. Install required libraries:
   ```bash
   pip install tensorflow numpy pandas matplotlib scikit-learn
   ```

3. Run the notebook:
   Open `notebook9fe2f24a6a.ipynb` in Jupyter or any IDE and execute all cells.

---

## 📈 Results

> Final model performance on validation set (example):
- **Validation MAE:** ~0.04
- **Validation MSE:** ~0.002

📌 *These values may vary depending on random seed and data split.*

---

## 📦 Model Saving & Loading (Optional)

```python
# Save
model.save("gre_prediction_model.h5")

# Load
from keras.models import load_model
model = load_model("gre_prediction_model.h5")
```

---

## 👨‍💻 Author

**Harsh Joshi**  
GitHub: [@hendrix0731](https://github.com/hendrix0731)

---

## 📜 License

This project is open-source under the **MIT License**. Feel free to fork, modify, and share.

