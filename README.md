# 🎓 Student Exam Score Prediction
## 📌 Problem Statement
Predict a student's exam score (out of 100) based on their study hours,
class attendance, and sleep habits using Linear Regression.

## 📦 Dataset Description
- **Source:** Manually created synthetic dataset
- **Rows:** 20 student records
- **Features:**
  | Feature          | Description                          |
  |------------------|--------------------------------------|
  | hours_studied    | Hours studied per day (1–10)         |
  | attendance_pct   | Class attendance percentage (55–98%) |
  | sleep_hours      | Average sleep per night (4–9 hrs)    |
  | practice_tests   | Number of practice tests taken (0–7) |
- **Target:** `exam_score` (0–100)

## 🤖 Model Used
- **Algorithm:** Linear Regression (scikit-learn)
- **Split:** 80% Train / 20% Test

## 📊 Results
| Experiment            | MAE   | R² Score |
|-----------------------|-------|----------|
| Original (3 features) | ~2.5  | ~0.97    |
| Removed sleep_hours   | ~3.1  | ~0.96    |
| Added practice_tests  | ~2.1  | ~0.98    |
| Full data (overfit)   | ~1.2  | ~0.99    |

## ✅ Conclusion
- `hours_studied` is the strongest predictor of exam performance.
- Adding `practice_tests` improved model accuracy meaningfully.
- Training on full data without splitting leads to overfitting.
- A proper train-test split gives a more realistic performance estimate.
```
