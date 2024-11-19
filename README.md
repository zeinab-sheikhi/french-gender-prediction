# French Gender Prediction Using Semantic and Phonological Distances

This project predicts the grammatical gender (masculine or feminine) of French words using a combination of **semantic distances** and **phonological distances**. The prediction model is implemented using the **XGBoost** algorithm, with comprehensive feature engineering and analysis.

---

## Features

- **Phonological Distance Analysis**:
  - Computes weighted Levenshtein distances to capture phonetic similarity between words.
  - Creates feature vectors for each word based on distances to the nearest masculine and feminine neighbors.

- **Semantic Distance Analysis**:
  - Extracts semantic features based on word embeddings or contextual relationships.
  - Quantifies the meaning-based similarity between words.

- **Hybrid Feature Engineering**:
  - Combines semantic and phonological features for improved prediction accuracy.

- **Ablation Studies**:
  - Evaluates model performance under three scenarios:
    1. Using only phonological features.
    2. Using only semantic features.
    3. Combining both semantic and phonological features.

---

## Methodology

1. **Data Preprocessing**:
    - Input dataset includes French words with their grammatical genders (`masculine` or `feminine`).
    - Words are grouped by gender for feature computation.

2. **Feature Engineering**:
    - **Phonological Features**: Based on weighted Levenshtein distances.
    - **Semantic Features**: Derived from contextual embeddings or related semantic metrics.
    - Combines both sets of features for a comprehensive feature vector.

3. **Model Training**:
    - XGBoost is used to train the model on the extracted features.
    - The model is evaluated using standard metrics (e.g., accuracy, F1-score).

4. **Ablation Studies**:
    - Tests the impact of phonological and semantic features separately and in combination.

---

## Results

The table below summarizes the average accuracy of the model under different feature types:

| **Feature Type** | **Average Accuracy** |
|-------------------|-----------------------|
| Phonological      | 0.8738               |
| Semantic          | 0.7254               |
| Both              | 0.8896               |

- **Key Finding**: Combining both phonological and semantic features achieves the highest accuracy (88.96%), demonstrating the complementary nature of these features.

---

## Dependencies

- Python 3.8+
- Pandas
- NumPy
- Joblib (for parallel processing)
- tqdm (for progress visualization)
- XGBoost

---

## How to Run

1. Clone the repository and navigate to the project directory:
   ```bash
   git clone <repository_url>
   cd french-gender-prediction
