**Wine Quality Prediction (Regression Modeling)**

This project explores predictive modeling on the Wine Quality dataset to estimate wine quality scores based on physicochemical properties. Several linear regression techniques were evaluated, including Lasso and Ridge regularization. Cross-validation was used to assess model performance more robustly.

---

**Dataset**

The dataset includes various features describing chemical properties of wine such as:

- Fixed acidity
- Volatile acidity
- Citric acid
- Residual sugar
- Chlorides
- Free sulfur dioxide
- Total sulfur dioxide
- Density
- pH
- Sulphates
- Alcohol

**Target variable:** `quality` (integer score from 3 to 8)

---

**Models Tested**

| Model              | Notes                                |
|-------------------|---------------------------------------|
| **Linear Regression** | Performed best overall                |
| Lasso Regression   | Higher error, underperformed          |
| Ridge Regression   | Similar to Lasso, did not improve MSE |

After comparing models, **Linear Regression** was selected as the final model based on performance.

---

**Cross-Validation Result**

- **5-Fold Cross-Validated MSE:** `-0.4366`  
  *(Note: The negative sign is due to scikit-learn’s scoring convention — actual MSE = **0.4366**)*
- **Root Mean Squared Error (RMSE):** ≈ **0.66** quality points

---

**Final Evaluation Summary (Linear Regression)**

| Alpha | Baseline MAE | Training MAE | Training R² | Testing MAE | Testing R² |
|-------|---------------|--------------|-------------|-------------|-------------|
| None  | 0.6837        | 0.5022       | 0.3587      | 0.5022      | 0.4096      |

- The **baseline model** used the mean quality score for all predictions.
- The **Linear Regression model** significantly outperformed the baseline.
- Lasso and Ridge regularization did not lead to improvements — possibly due to the relatively small feature set and minimal overfitting.
