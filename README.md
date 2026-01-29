# Kickstarter Project Success Prediction

This project builds and evaluates machine learning models to predict Kickstarter project success using only pre-launch data.

# Objective
why is this project matter?

To classify whether a Kickstarter project will succeed or fail before launch, helping creators set realistic goals and enabling better decision-making.

# Dataset

Historical Kickstarter campaign data including:
+ Funding goals
+ Campaign duration
+ Category and country
+ Launch timing
+ Project title features

# Approach
- Exploratory Data Analysis (EDA)
- Feature engineering with context-aware signals (e.g., goal realism, fundraising pressure)
- Baseline Logistic Regression model
- Improved Logistic Regression with selected features
- XGBoost model to capture non-linear relationships
- Evaluation using ROC–AUC and cross-validation for stability

 # Key Results
+ Baseline Logistic Regression ROC–AUC ≈ 0.64
+ XGBoost ROC–AUC ≈ 0.68
- Cross-validation confirms stable and generalizable performance

# Conclusion

Non-linear models combined with thoughtful feature engineering significantly improve the prediction of Kickstarter project success using pre-launch data alone.

⸻

 # Setup:
 1. Create and activate a virtual environment
+ macOS / Linux
 python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt

+ Windows
python -m venv .venv
.venv\Scripts\Activate
pip install --upgrade pip
pip install -r requirements.txt

