# ZeroShot-NewsClassifier

This project demonstrates a zero-shot text classification approach on the AG-News dataset using pretrained language models. Instead of training a classifier, it compares input news articles with predefined label descriptions using **cosine similarity between sentence embeddings**.

## 🚀 Project Summary

We classify AG-News dataset samples into four categories — **World**, **Sports**, **Business**, and **Sci/Tech** — without training any model. We use sentence embeddings from two types of models:

1. **Baseline BERT**: `bert-base-uncased`
2. **Contrastively Trained BERT**: `princeton-nlp/sup-simcse-bert-base-uncased`

Predictions are made by computing cosine similarity between sentence embeddings and label description embeddings.

## 🧠 Concept Used

This approach is based on:
- **Zero-shot learning**: No model training or fine-tuning is involved.
- **Sentence Embedding Similarity**: Use `CLS` token embeddings from BERT/SimCSE.
- **Cosine Similarity**: Measure closeness of news content to label descriptions.

### Label Descriptions
We define the labels using natural language sentences:
- `"This text is about world news."`
- `"This text is about sports."`
- `"This text is about business."`
- `"This text is about science and technology."`

Each article is compared against these label descriptions using cosine similarity of their embeddings.

## 🧪 Models Used

| Model                            | Description                               |
|----------------------------------|-------------------------------------------|
| `bert-base-uncased`              | Standard pretrained BERT model            |
| `princeton-nlp/sup-simcse-bert`  | Contrastively trained for better similarity|

## 📊 Results

| Model         | Accuracy (%) |
|---------------|--------------|
| BERT          | ~ Baseline   |
| SimCSE        | ~ Higher     |


## 📁 Files

- `AdvanceML_Q2.ipynb` – Main notebook containing code and evaluation.

## 📚 Dataset

- [AG-News Dataset](https://www.di.unipi.it/~gulli/AG_corpus_of_news_articles.html)
  - Four classes: World, Sports, Business, Sci/Tech
  - Only 5,000 samples used for demonstration

## 💡 How to Run

```bash
pip install torch transformers scikit-learn pandas tqdm
```
Then run the Jupyter notebook AdvanceML_Q2.ipynb.

## 🧩 Extensions
- Try other contrastive models like SBERT (all-MiniLM-L6-v2)

- Use more descriptive label prompts

- Evaluate with full dataset

## Crreated By 
**Lovy Verma**
