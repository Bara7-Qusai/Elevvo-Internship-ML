

#  Student Score Prediction – Model Evaluation

## Model Performance Comparison

The linear regression model was trained on two versions of the dataset: one including outliers and one with outliers removed.

The model trained on the original dataset (with outliers) achieved an **R² score of 0.6678**, meaning it explains approximately 66.8% of the variance in students' exam scores. Its **Mean Squared Error (MSE) was 5.0826**, indicating a moderate level of prediction error.

After removing outliers, the model performance improved significantly. The **R² score increased to 0.8750**, meaning the model now explains 87.5% of the variance in exam scores. Additionally, the **MSE dropped to 1.2553**, reflecting a substantial reduction in prediction error.

These results clearly demonstrate that outliers had a strong negative impact on the regression model. Removing them greatly improved accuracy, stability, and overall predictive reliability.

