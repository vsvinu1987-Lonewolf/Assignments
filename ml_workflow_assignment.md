ML Workflow Assignment
Task 1: Label and Data Leakage Identification
Label

Column: repeat_purchase_flag

Justification: This is the label because it represents the exact binary outcome (whether the customer made a repeat purchase within 30 days) that the model is being trained to predict.

Data Leakage

Column: discount_used_on_repeat_order

Justification: Including this as a feature introduces data leakage because you would only know the discount applied to a repeat order after the repeat order has actually occurred, meaning this information would not be available at the time you are making the prediction.

Task 2: Missed ML Workflow Steps
Before jumping straight to training a complex model like gradient boosting, the following two critical steps should be completed:

1. Data Preprocessing and Exploratory Data Analysis (EDA)

Why it matters: Raw data is rarely ready for modeling. Before training, you must audit the dataset to handle missing values, encode categorical variables, scale numerical features, and explicitly remove leaky features (like discount_used_on_repeat_order). Skipping this step guarantees the model will either fail to train or will learn patterns based on flawed, biased, or "cheating" data.

2. Establishing a Simple Baseline Model

Why it matters: Before investing time and computational resources into a complex, "black-box" model like gradient boosting, you should train a highly interpretable, simple baseline (such as predicting the majority class or using a basic Logistic Regression). This gives you a minimum performance threshold to prove whether the complex model actually adds measurable value.