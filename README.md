# CANCEL-HOTEL-BOKKING-CASE-STUDY
This project aims to help INN Hotels Group reduce revenue loss caused by high booking cancellation rates (~33%), by building a predictive Machine Learning model that identifies high-risk bookings before they cancel. The project follows a complete Data Science lifecycle including EDA, hypothesis testing, feature engineering, modeling, evaluation, probability-cutoff tuning, and deployment.
🚀 Project Highlights

✔ Analyzed 27K+ past bookings and 3.5K+ new bookings ✔ Performed detailed EDA, numerical profiling, and categorical analysis ✔ Statistical validation using t-tests and Chi-square ✔ Engineered impactful features: stay duration, arrival/departure weekday, seasonality ✔ Applied outlier treatment, PowerTransformer, and scaling ✔ Built multiple ML models: Logistic Regression

Decision Tree

Random Forest

XGBoost

Soft Voting Ensemble (Final Model) ✔ Tuned probability cutoff using Youden’s Index to maximize recall ✔ Deployed final model using joblib, ready for Streamlit or production integration ✔ Provided actionable business recommendations for hotel revenue optimization

📊 Business Problem

INN Hotels faces:

33% booking cancellation rate

Only 20% of cancelled bookings get rebooked

Result: major revenue leakage & inventory mismanagement

The goal is to build a system that can predict cancellations at booking time, allowing the hotel to:

Apply targeted retention strategies

Offer discounts or reminders

Secure deposits for high-risk customers

Use overbooking optimally

Improve room allocation and staffing decisions

🔍 Key Insights from EDA

Guests with higher lead time (book early) cancel more often

Higher room price shows a strong cancellation link

Certain arrival months have more cancellations (seasonal impact)

Guests with no special requests cancel more than those engaged

Longer stay duration increases uncertainty → more cancellations

Online channel bookings cancel more frequently

Statistical tests confirm these patterns (p < 0.05 for all major variables).

🧠 Modeling & ML Approach Models Tested

Logistic Regression (baseline)

Decision Tree

Random Forest

XGBoost

Voting Ensemble (Decision Tree + XGBoost)

🔥 Final Selected Model: Voting Classifier

Chosen because it gives:

High accuracy (~83%)

High cancellation recall (~78%)

Strong ROC AUC (~0.88–0.89)

A lower cutoff probability (~0.3) improves recall (business priority) while keeping precision reasonable.

🛠 Tech Stack

Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, Plotly, SciPy, Joblib, Streamlit (optional deployment)

🧩 Model Deployment

The following are saved for production/scoring usage:

transformer.joblib – PowerTransformer for numeric features

final_model.joblib – Voting classifier

feature_list.pkl – Expected feature order

This allows integration with:

Streamlit app (interactive prediction)

Hotel booking systems

Automated CRM workflows

🏁 Results

~78% of cancellations detected BEFORE they happen

Helps reduce last-minute no-shows

Supports dynamic pricing, targeted offers, and better overbooking strategy

Leads to significant operational and revenue improvements

🧩 How to Use This Project

Clone the repository

Install dependencies using pip install -r requirements.txt

Run the notebook step-by-step

Use joblib files for real-time API/Streamlit scoring

🎯 Business Impact

This system gives hotel management the ability to:

Identify at-risk bookings early

Actively prevent cancellations

Optimize revenue

Improve inventory management

Enhance customer engagement

Reduce operational uncertainty
