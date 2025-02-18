# Shopping prediction model

## Overview
This project implements a machine learning model to predict whether online shopping customers will complete a purchase based on their browsing behavior. Using a k-nearest neighbors classifier, the system analyzes various user session attributes to predict purchase likelihood, achieving meaningful results on both sensitivity (true positive rate) and specificity (true negative rate) metrics.

## Project Background
Developed as part of Harvard's CS50AI course, this project addresses a real-world business challenge: predicting customer purchase intent during online shopping sessions. The model can be used to identify potential customers who might need additional engagement (like special offers) to complete their purchase.

## Features
- Processes multiple user behavior metrics including:
  - Page visit counts (Administrative, Informational, Product-related)
  - Time duration analysis
  - Bounce rates and exit rates
  - Special day proximity
  - User type classification
  - Weekend vs weekday behavior
- Implements k-nearest neighbors algorithm (k=1)
- Evaluates model performance using sensitivity and specificity metrics
- Handles various data types and preprocessing requirements

## Technologies Used
- Python 3.12
- pandas (for data manipulation)
- scikit-learn (for machine learning implementation)
- Key libraries: KNeighborsClassifier, train_test_split


## Implementation Details
The project consists of three main components:

1. **Data Loading and Preprocessing** (`load_data`):
   - Converts categorical data to numerical format
   - Handles multiple data types (int, float)
   - Processes temporal and boolean features

2. **Model Training** (`train_model`):
   - Implements k-nearest neighbors classifier
   - Uses single nearest neighbor for classification

3. **Model Evaluation** (`evaluate`):
   - Calculates sensitivity (true positive rate)
   - Calculates specificity (true negative rate)

## Results
The model achieves:
- True Positive Rate: 41.02%
- True Negative Rate: 90.55%

These results show strong performance in identifying non-purchasing customers while maintaining reasonable accuracy in identifying likely purchasers.

## Running the Project
1. Clone the repository
2. Install requirements:
   ```bash
   pip install scikit-learn pandas
   ```
3. Run the predictor:
   ```bash
   python shopping.py shopping.csv
   ```

## Learning Outcomes
- Implementation of k-nearest neighbors algorithm
- Handling imbalanced datasets
- Working with real-world data preprocessing challenges
- Understanding and implementing proper model evaluation metrics

## Acknowledgements
- Dataset provided by Sakar, C.O., Polat, S.O., Katircioglu, M. et al. Neural Comput & Applic (2018)
- Project structure and requirements from Harvard's CS50AI course
