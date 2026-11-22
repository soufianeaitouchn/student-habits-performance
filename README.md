# Student Habits vs Academic Performance

A machine learning project that predicts a student's exam score from their daily habits (study time, attendance, mental health, sleep, part-time job).

## Project structure

```
student-habits-performance/
├── data/student_habits_performance.csv   # dataset (1000 students)
├── notebooks/notebook.ipynb              # analysis + model training
├── models/best_model.pkl                 # saved best model
├── app.py                                # Streamlit web app
└── requirements.txt                      # libraries
```

## Installation

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Usage

**Notebook:** open `notebooks/notebook.ipynb` in VS Code, select the `.venv` kernel, then click **Run All**.

**Web app:**

```powershell
.\.venv\Scripts\python.exe -m streamlit run app.py
```

Then open http://localhost:8501.

## Results

| Model             | RMSE | R²   |
|-------------------|------|------|
| Linear Regression | 8.05 | 0.78 |
| Random Forest     | 8.54 | 0.75 |
| Decision Tree     | 9.11 | 0.72 |

The best model is **Linear Regression**: it predicts the exam score with an average error of about 8 points.
**Study hours** is by far the most important factor (correlation 0.83), followed by **mental health** (0.32).
