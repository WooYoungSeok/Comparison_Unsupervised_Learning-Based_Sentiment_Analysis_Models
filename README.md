# Comparison of Unsupervised Learning-Based Sentiment Analysis Models

## Project Overview
This project evaluates and compares three unsupervised sentiment analysis models—**TextBlob**, **VADER**, and **Pattern**—using a Twitter dataset. The goal was to examine their performance, particularly in relation to data preprocessing and label definition.

---

## Data Link
https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis

---

## Key Features
- **Sentiment Analysis Models:**
  - **TextBlob:** Provides sentiment polarity scores using pre-trained NLP tools.
  - **VADER:** Optimized for social media, considering elements like abbreviations, emojis, and punctuation.
  - **Pattern:** Offers sentiment analysis and other NLP functions, expressing sentiment as polarity scores.

- **Dataset:** Twitter posts, rich in diverse emotional expressions.
- **Preprocessing Impact:** Compared model performance before and after text preprocessing.

---

## Methodology
### 1. Data Exploration and Preprocessing
- **Initial Cleaning:**
  - Removed unnecessary columns and irrelevant sentiments.
  - Renamed columns for clarity (`sentiment`, `text`).
  - Balanced sentiment classes (`Positive`, `Neutral`, `Negative`).
- **Text Preprocessing:**
  - Removed special characters but retained emojis for sentiment context.
  - Applied stop-word filtering and case normalization.
  - Eliminated duplicates to reduce noise.

### 2. Sentiment Analysis Models
- **TextBlob:**
  - Built on NLTK and Pattern, evaluates polarity of text.
  - Outputs scores between -1.0 (negative) and +1.0 (positive).
- **VADER:**
  - Tailored for social media, considers slang, capitalization, and punctuation.
- **Pattern:**
  - Evaluates text polarity with a range similar to TextBlob.

### 3. Evaluation
- Models' performance was compared across:
  - Raw data vs. preprocessed data.
  - Label ranges for neutrality (`|polarity| ≤ 0.1` yielded optimal results).
- Performance metrics include accuracy and F1-scores.

---

## Results
- **Neutral Label Definition:**
  - Optimal range for "Neutral" polarity: `|polarity| ≤ 0.1`.
- **Impact of Preprocessing:**
  - Accuracy decreased for all models post-preprocessing due to information loss in short-text datasets.
  - Preprocessing proved less critical for this dataset type.
- **Model Comparison:**
  - **Pattern** outperformed VADER and TextBlob, achieving the highest accuracy both before and after preprocessing.
  - Surprisingly, VADER, designed for social media, did not surpass Pattern.

---

## Conclusion
- The project highlights the importance of considering dataset characteristics (e.g., short-text nature) when applying preprocessing techniques.
- Pattern was identified as the best-performing model, challenging assumptions about VADER's superiority for social media.
- Future work could explore more diverse datasets and additional models to validate these findings.

---

## References
1. **Guo, Y., Hu, C., & Yang, Y.** (2023). Predict the Future from the Past? On the Temporal Data Distribution Shift in Financial Sentiment Classifications. _arXiv preprint arXiv:2310.12620_.
2. **Kevin, M.** (2024). Twitter Sentiment Analysis – Logistic Regression. _Kaggle_. [Link](https://kaggle.com/code/kevinmorgado/twitter-sentiment-analysis-logistic-regression)
3. **NLTK Documentation.** (2024). [Link](https://www.nltk.org/_modules/nltk/sentiment/vader.html)
4. **Pattern.en Documentation.** (2024). [Link](https://digiasset.org/html/pattern-en.html#sentiment)
5. **TextBlob GitHub.** (2024). [Link](https://github.com/sloria/textblob)

---

## Contact
- **Author:** Yeongseok Woo  
- **Affiliation:** AI Convergence Department, Sungkyunkwan University  
- **Email:** [your-email@example.com]
