# Ridge and Lasso Regression for Baseball Player Salary Prediction

This project implements and compares three regression models—Linear Regression, Ridge Regression, and Lasso Regression—to predict the salaries of baseball players based on their performance statistics and career achievements.

## 📁 Dataset

The dataset used is `Hitters.csv`, which contains information about 322 baseball players and 20 features, including:

- **Performance metrics** from the 1986 season (e.g., `HmRuns`, `Hits`)
- **Career totals** (e.g., `CHits`, `CRuns`)
- **Categorical variables**: `League`, `Division`, `NewLeague`
- **Target variable**: `Salary` (player earnings)
The explanation of the data features can be found in `Hitters Data Legend.xlsx`

## 🛠️ Preprocessing Steps

1. **Handling Categorical Variables**:
   - Converted `League`, `Division`, and `NewLeague` into dummy variables.

2. **Missing Values**:
   - Removed rows with missing `Salary` values for model training and testing.

3. **Feature Scaling**:
   - Standardized features using `StandardScaler` to ensure equal contribution to the model.

## 📊 Exploratory Data Analysis (EDA)

- Visualized the distribution of salaries.
- Analyzed correlations between features and the target variable.
- Checked for multicollinearity using a heatmap.

## 🧪 Models Implemented

### 1. Linear Regression
- Used as a baseline model.
- No regularization applied.

### 2. Ridge Regression
- Uses L2 regularization.
- Hyperparameter `alpha` tuned via `RidgeCV` with repeated K-Fold cross-validation.

### 3. Lasso Regression
- Uses L1 regularization.
- Hyperparameter `alpha` tuned via `LassoCV` with repeated K-Fold cross-validation.

## 📈 Evaluation Metrics

- **Root Mean Squared Error (RMSE)**
- **R² Score** (Training and Testing)

## 🏆 Model Comparison

Ridge Regression performed the best in this case, followed by Lasso.

## Predicting Missing Salaries

The trained Ridge model was used to predict missing `Salary` values in the original dataset, demonstrating its practical utility.
