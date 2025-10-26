# 🧠 AI-Powered Career Guidance Platform

## 📘 Introduction

This project is an **interactive Streamlit web application** designed to help students in their academic and career journey using **Machine Learning**.  
It leverages data-driven insights to provide personalized recommendations through three core modules:

- 🎯 **Skill Recommender** – Suggests relevant technologies and skills based on a student’s current competencies and field of interest.  
- 👨‍🏫 **Mentor Matcher** – Recommends professors for mentorship using feedback, experience, and past mentee performance.  
- 💼 **Placement Predictor** – Predicts a student’s placement tier using academic, coding, and soft-skill indicators.

The goal of this project is to create an intuitive, AI-assisted career advisory tool combining real and simulated data, ML models, and an easy-to-use interface.

---

## 🧩 Datasets

- **Student Dataset:** Includes academic performance, projects, internships, coding profile, and placement details.  
- **Professor Dataset:** Contains mentorship effectiveness, feedback ratings, and experience metrics.  
- The datasets are merged, cleaned, and transformed into structured, ML-ready formats.

---

## ⚙️ Project Overview

This end-to-end system comprises the following components:

1. **Skill Recommender** – Computes a skill match percentage and suggests technologies to learn.  
2. **Mentor Matcher** – Recommends professors based on experience, feedback, and student outcomes.  
3. **Placement Predictor** – Uses a **Random Forest Classifier** trained on academic and skill-based data to predict placement tiers.  
4. **Streamlit App** – Provides a unified, interactive interface to access all modules.  
5. **Deployment Ready** – Designed for easy integration with backends like Flask or FastAPI.

---

## Model Download and Directory Structure

### Trained Models:

- Models are saved using `joblib` and used directly in the Streamlit app.

### Directory Structure:

```
career-assistant/
│
├── tech_recommender.py              # Skill matching logic
├── mentor_matcher_app.py            # Streamlit app (UI for skill, mentor, placement)
├── placement_rf_classifier.pkl      # Trained Random Forest Classifier (placement prediction)
├── scaler_for_classifier.pkl        # StandardScaler used for feature preprocessing
├── Enhanced_Professor_Database.csv  # Professor dataset with quality metrics
├── Student_Data_With_Extras.xlsx    # Combined and engineered student dataset
├── README.md                        # Project documentation
└── requirements.txt                 # List of Python dependencies
```

## Setup Instructions

### Step 1: Create a Virtual Environment

```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Run the Application

```bash
streamlit run mentor_matcher_app.py
```

The app will be hosted at `http://localhost:8501/`.

## Application Modules

### Skill Recommender

- Input: Field of interest, existing skills
- Output: Match score (%), Recommended skills

### Mentor Matching

- Input: Student’s field of interest
- Output: Top N matched professors based on:
  - Feedback Rating
  - Years of Experience
  - Past Mentee Performance
  - Behavior Rating

### Placement Tier Predictor

- Input: Coding rating, GPA, projects, certifications, communication rating, etc.
- Model: Random Forest Classifier
- Output: Placement tier label (Tier 1–4)

## Model Architecture

The placement model uses the Random Forest algorithm, which is suitable for high-dimensional tabular data with both categorical and continuous features.

### Important Features:

- Coding_Profile_Rating
- Major_Projects and Mini_Projects
- Internships and Hackathons
- Skill_Match_Score (from recommender)
- Communication and Soft Skill Ratings

## Data Preprocessing

- Filled missing values using domain-aware defaults
- Engineered categorical encodings and normalized numerical values
- Created custom labels for placement tiers
- Scaled feature vectors using `StandardScaler`

## Conclusion

This AI-powered platform provides a comprehensive solution for skill analysis, career mentorship, and placement prediction. It demonstrates practical use of machine learning in education and can be expanded for institutional use with more real-world data and integrations.

## Future Enhancements

- Improve UI with animations and interactive charts
- Integrate login/user tracking and history saving
- Deploy to cloud platforms (Streamlit Cloud, Render, Heroku)
- Build frontend in React and backend in FastAPI for scalability

✨ Author

Vipul Kumar
📧 Email: vipulkr20602@gmail.com
🔗 LinkedIn: https://www.linkedin.com/in/vipul-kumar-212445256/
🐙 GitHub: https://github.com/Vipul20K

