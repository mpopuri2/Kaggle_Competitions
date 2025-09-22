
# Titanic Survival Prediction 🚢

This project predicts the survival of passengers aboard the Titanic using machine learning techniques. 
It is based on the classic Kaggle competition: [Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic).

---

## **Project Overview**
The Titanic dataset contains demographic and travel information for passengers aboard the RMS Titanic. 
The goal is to build a model that predicts whether a passenger survived or not.

The model is evaluated based on prediction accuracy, with the Kaggle public leaderboard showing performance scores.

> **My first submission:**  
> - **Score:** `0.74641` (74.64% accuracy)  
> - **Rank:** Reached the leaderboard successfully 🎉

---

## **Repository Structure**

```
titanic-survival-prediction/
│
├── Titanic_Survival_Prediction.ipynb   # Jupyter Notebook with EDA, feature engineering, and model building
├── Submission.csv                       # Final predictions for Kaggle submission
├── README.md                            # Project documentation (this file)
└── data/                                 # Folder for datasets (train.csv, test.csv)
```

---

## **Files Description**
| File | Description |
|------|-------------|
| `Titanic_Survival_Prediction.ipynb` | The main notebook containing data exploration, visualization, feature engineering, and model training using XGBoost and other ML models. |
| `Submission.csv` | Output file submitted to Kaggle. Contains `PassengerId` and `Survived` columns with final predictions. |
| `data/` | Directory to store raw and processed datasets (`train.csv` and `test.csv`). |
| `README.md` | Documentation for the project and instructions on how to reproduce results. |

---

## **Tech Stack**
- **Python** (v3.10+)
- **Libraries**:
  - pandas
  - numpy
  - matplotlib / seaborn
  - scikit-learn
  - xgboost

---

## **Workflow**
### 1. Data Exploration
- Load and inspect datasets (`train.csv`, `test.csv`)
- Handle missing values in features like `Age`, `Cabin`, and `Embarked`
- Visualize patterns (e.g., survival rates by gender, class, and age)

### 2. Feature Engineering
- Extract useful features from `Name` and `Ticket`
- Convert categorical variables like `Sex` and `Embarked` into numerical format
- Create new features such as `FamilySize` and `IsAlone`

### 3. Model Building
- Models considered:
  - Logistic Regression
  - Random Forest
  - XGBoost Classifier (final choice)
- Performed hyperparameter tuning using GridSearchCV

### 4. Evaluation
- Used cross-validation to evaluate model performance
- Selected **XGBoost** for best accuracy and generalization

### 5. Submission
- Generated predictions on the test set
- Created `Submission.csv` for Kaggle upload

---

## **How to Run the Project**
1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/titanic-survival-prediction.git
   cd titanic-survival-prediction
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Add datasets:**
   - Download `train.csv` and `test.csv` from Kaggle.
   - Place them inside the `data/` directory.

4. **Run the notebook:**
   ```bash
   jupyter notebook Titanic_Survival_Prediction.ipynb
   ```

5. **Generate predictions:**
   - After running all cells, the notebook will output a `Submission.csv` file.
   - Upload this file to Kaggle to check your leaderboard score.

---

## **Leaderboard Result**
| Submission Date | Score    | Notes                |
|-----------------|----------|----------------------|
| First submission | 0.74641  | Base model with feature engineering |

---

## **Future Improvements**
- Try **Ensemble Learning** (stacking, bagging)
- Experiment with advanced feature engineering (e.g., natural language processing on `Name`)
- Use deep learning models for comparison
- Apply SHAP or LIME for model explainability

---

## **Acknowledgements**
- [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- Open-source libraries and Kaggle discussions for insights and techniques.
