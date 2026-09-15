# Redmi 6 Feedback Sentiment Analysis

A Natural Language Processing (NLP) project for analyzing **Redmi 6 customer reviews and feedback** and classifying them as **Positive, Neutral, or Negative**.

## 🛠️ Technologies

* Python
* Pandas
* NLTK / VADER
* PyTorch
* Hugging Face Transformers

## 🔄 Workflow

```text
Dataset
   ↓
Extract Review Columns
   ↓
Merge Feedback
   ↓
Sentiment Analysis
   ↓
Positive / Neutral / Negative
```

## 📌 Features

* Identifies review, comment, and feedback columns.
* Combines multiple text columns into one.
* Performs sentiment analysis using **VADER**.
* Performs sentiment classification using a **Transformer model**.
* Compares sentiment results from different approaches.

## 💻 Example

```python
df["Merge_Column"] = df.apply(
    merge_columns,
    axis=1,
    args=(review_columns,)
)

df["sentiments_nltk"] = df["Merge_Column"].apply(
    analyze_sentiment
)
```

## 📊 Output

| Review              | Sentiment |
| ------------------- | --------- |
| Excellent phone     | Positive  |
| Battery is terrible | Negative  |
| The phone is okay   | Neutral   |
