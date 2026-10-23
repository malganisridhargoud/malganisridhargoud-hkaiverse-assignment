# AI Exercise 5 — Machine Learning

## Prompt

> Explain data leakage with a simple train/test example and propose a prevention check.

## Model and date

- Model: GPT-6
- Date: 2026-10-23

## Output summary

The model defined leakage as training or evaluating with information that would not be available at prediction time. It recommended splitting data before fitting preprocessing and fitting transformations only on the training data.

## Verification

The suggestion was compared against standard machine-learning practice:

- Split the dataset into train and test sets first.
- Fit preprocessing steps such as scaling or imputation on the training subset only.
- Apply the learned transformation to the test subset.
- Do not include target-derived features or future information in the input features.

## Result

This advice matches standard practice for preventing data leakage. The record stays at educational-example level and does not claim an executed pipeline or a production model evaluation.
