# OpportunityCheck implementation plan

## First milestone

Build a reproducible training pipeline before the interface. Record the data source and terms, remove duplicate or closely related postings before splitting, and keep a final test set untouched during model selection.

Acceptance criteria:

- A script produces deterministic train, validation, and test splits.
- A simple baseline and TF-IDF logistic regression model are compared.
- Fraud-class precision, recall, F1, and a confusion matrix are reported.
- The report documents dataset age, class imbalance, and likely failure cases.

## Second milestone

Add a prediction interface that accepts a job description and returns a score with influential text features. Explain that these are model signals rather than verified facts about a company.

Acceptance criteria:

- Empty and excessive input receive clear validation messages.
- A saved pipeline can be loaded without retraining on every request.
- The interface has fictional sample postings and displays model limitations.
- Tests cover input handling, deterministic predictions, and output shape.

## Third milestone

Deploy a Streamlit demo. Add screenshots, the real demo URL, reproducible run commands, and actual evaluation results to the README only after they exist.
