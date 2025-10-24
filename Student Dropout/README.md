1. SVM (Support Vector Machine)

Performance:

Performs well with smaller to medium-sized datasets.

Effective in high-dimensional spaces (many features).

Challenges:

Sensitive to parameter tuning (C, kernel, gamma).

Computationally expensive on large datasets.

Not naturally suited for multi-class classification; requires strategies like one-vs-one or one-vs-rest.

Expected Behavior:

With proper hyperparameter tuning, SVM can accurately separate dropout, graduate, and enrolled classes.

May struggle if classes overlap significantly.

2. Logistic Regression

Performance:

Fast, interpretable, and good for linearly separable data.

Provides probability estimates for each class.

Challenges:

Limited performance for non-linear relationships.

Sensitive to multicollinearity among features.

Expected Behavior:

Gives baseline performance.

Works well with well-scaled numeric features and one-hot encoded categorical variables.

3. Decision Tree

Performance:

Simple, interpretable, and can capture non-linear patterns.

Handles categorical and numerical data.

Challenges:

Prone to overfitting, especially with deep trees.

Sensitive to small changes in the data.

Expected Behavior:

May achieve high training accuracy but can overfit if not pruned or limited in depth.

Easy to visualize and understand decision rules.

4. MLP (Multi-Layer Perceptron)

Performance:

Can capture complex, non-linear relationships.

Flexible with architecture (hidden layers, neurons, activation functions).

Challenges:

Requires careful tuning (learning rate, hidden layers, alpha, activation).

Sensitive to feature scaling.

Longer training time, especially on larger datasets.

Expected Behavior:

Can outperform simpler models if enough data and proper tuning are available.

Might overfit if regularization is insufficient.

5. K-Means Clustering (Unsupervised)

Performance:

Useful for exploratory analysis and grouping similar students.

Provides approximate accuracy by mapping clusters to actual classes.

Challenges:

No true supervision; accuracy is approximate.

Sensitive to initialization and number of clusters.

Works best with well-scaled features.

Expected Behavior:

Can identify groups of students with similar characteristics.

Helps understand patterns but is not as accurate as supervised models for prediction.

6. Random Forest

Performance:

Ensemble of decision trees; reduces overfitting.

Handles non-linear relationships and high-dimensional data.

Robust to outliers and missing values.

Challenges:

Less interpretable than single decision trees.

Can be computationally expensive for very large forests or datasets.

Expected Behavior:

Often achieves the highest or near-highest accuracy.

Stable predictions across different random seeds.

Works well even if some features are noisy or irrelevant.

Overall Challenges & Considerations

Class Imbalance: Needs balancing (e.g., SMOTE) to prevent bias toward majority class.

Feature Selection: Reduces noise and improves performance; top 10 features were used.

Scaling: Required for SVM and MLP to converge properly.

Overfitting vs Generalization: Tree-based and neural network models can overfit; hyperparameter tuning is critical.

Interpretability vs Accuracy: Simpler models (Logistic, Decision Tree) are interpretable; complex models (MLP, Random Forest) are more accurate but less interpretable.
