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

 ## Setup:
 1. Create and activate a virtual environment:
 
 
+ macOS / Linux

 ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/bin/activate
    pip install --upgrade pip
    pip install -r requirements.txt
    ```

WindowsOS type the following commands :

- Install the virtual environment and the required packages by following commands.

   For `PowerShell` CLI :

    ```PowerShell
    pyenv local 3.11.3
    python -m venv .venv
    .venv\Scripts\Activate.ps1
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    For `Git-bash` CLI :
  
    ```BASH
    pyenv local 3.11.3
    python -m venv .venv
    source .venv/Scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt
    ```

    **`Note:`**
    If you encounter an error when trying to run `pip install --upgrade pip`, try using the following command:
    ```Bash
    python.exe -m pip install --upgrade pip
    ```


   
## Usage

In order to train the model and store test data in the data folder and the model in models run:

**`Note`**: Make sure your environment is activated.

```bash
python example_files/train.py  
```

In order to test that predict works on a test set you created run:

```bash
python example_files/predict.py models/linear_regression_model.sav data/X_test.csv data/y_test.csv
```

## Limitations

Development libraries are part of the production environment, normally these would be separate as the production code should be as slim as possible.


---

## Handling Merge Conflicts in Jupyter Notebooks

When working in teams, `.ipynb` files can cause messy merge conflicts because they’re JSON-based.  
We use **nbdime** to make this easy.

### Setup (run once)
```bash
nbdime config-git --enable
```

### When a conflict happens
```bash
nbdime mergetool
```

A web interface will open showing both notebook versions side by side.
Choose what to keep, save and close tool, then:
```bash
git add your_notebook.ipynb
git commit -m "Resolved notebook conflict"
```
That’s it — clean merges for notebooks!