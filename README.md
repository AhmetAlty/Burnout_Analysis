# Technical Project: Remote Work Burnout Analysis & Prediction
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/AhmetAlty/Burnout_Analysis/blob/main/Burnout_Analysis.ipynb)
[![View in nbviewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.org/github/AhmetAlty/Burnout_Analysis/blob/main/Burnout_Analysis.ipynb)

> [!NOTE]
> This project was developed via **Antigravity AI**.  
> 🎓 **[Read the Senior Evaluation Report (Audit)](docs/evaluation_report.md)** - A multi-perspective analysis (Junior vs. Senior vs. Recruiter).
> The analysis is based on **Synthetic Data** to ensure realistic behavioral modeling.

## 🚀 Overview
This repository contains a test and development-focused analysis and predictive modeling project focused on occupational health in remote work environments. The project is based on the [Work From Home Employee Burnout Dataset](https://www.kaggle.com/datasets/sonalshinde123/work-from-home-employee-burnout-dataset) from Kaggle.

## 📊 Key Findings
- **Sleep Deprivation & Burnout:** Sleep duration is the strongest inversely correlated factor with burnout risk.
- **The Screen Intensity Threshold:** Employees exceeding 9 hours of screen time show a disproportionate increase in burnout scores.
- **Productivity Paradox:** High task completion rates do not necessarily indicate well-being; they often precede a "High Risk" burnout phase when coupled with low sleep.

## 🛠️ Tech Stack
- **Analysis:** `Pandas`, `NumPy`, `SciPy`
- **Visualization:** `Seaborn`, `Matplotlib`, `Plotly` (Interactive EDA)
- **Machine Learning:** `XGBoost`, `LightGBM`, `Scikit-Learn`
- **Explainable AI (XAI):** `SHAP` (TreeExplainer)

## 🏗️ Methodological Rigor
Acknowledging the **Class Imbalance** (High Risk at ~5%), the following senior-level mitigations were implemented:
- **Stratified Splitting:** Ensuring representative samples in both training and validation sets.
- **Recall (Sensitivity) Focus:** Since the cost of missing a high-risk employee (False Negative) is high, the model evaluation prioritizes **Recall** for the 'High' class over simple accuracy.
- **Advanced Ratios:** Utilizing behavioral indexes like `Sleep Efficiency` to sharpen decision boundaries for minority classes.

> [!TIP]
> **AI as a Strategic Senior Partner:** Beyond code generation, **Antigravity AI** was utilized in this project as a "Senior Evaluator." It provided multi-perspective feedback (Junior vs. Senior vs. Interviewer) and strategic advice, showcasing an unconventional use of AI as a high-level consultant for project auditing and career-oriented refinement.

## 💻 Installation & Usage
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```bash
   jupyter notebook Burnout_Analysis.ipynb
   ```

## 📝 License
MIT License. Feel free to use and contribute.
