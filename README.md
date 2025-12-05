# Classifying and Summarizing Arabic Text: Traditional vs Modern Approaches
Access the full notebook here: [Open in Google Colab](https://colab.research.google.com/drive/1_fS4Rv9TwqE3FOGntYervhkFKBeOY5mv?usp=sharing)

## Project Overview
This project compares traditional machine learning, deep learning, and transformer-based models for two key Arabic NLP tasks: text classification and text summarization.
We evaluate SVM and TF-IDF (traditional), BiLSTM/RNN and mT5 (deep learning), and AraBERT + BERT extractive summarization (transformers) to understand their strengths, limitations, and suitability for Arabic text.

## Dataset
We use the [Arabic Articles Dataset](https://github.com/alaybaa/ArabicArticlesDataset), which contains news articles from 10 categories (e.g., Sport, Art, Health, Politics). Each article includes a title and body text, making the dataset suitable for both classification and summarization tasks.

## Arabic NLP Challenges
Arabic presents unique challenges such as rich morphology, orthographic ambiguity, clitics, dialect variation, and limited annotated datasets. These factors require careful preprocessing and model adaptation to achieve reliable NLP performance.

## Comparative Performance Summary
### Text Classification – Model Comparison
| Model        | Overall Accuracy | Weighted F1 | Notes |
|--------------|------------------|-------------|-------|
| **AraBERT (Transformer)** | **94.25%** | **0.94** | Highest performance; tested on smaller sample (N=400). |
| **SVM (Traditional)** | 93.9% | 0.94 | Strong baseline; fast and resource-efficient. |
| **BiLSTM (Deep Learning)** | 92.6% | 0.93 | Good at sequence modeling; moderate compute needs. |
| **RNN (Deep Learning)** | 73.3% | 0.70 | Struggles with long dependencies; weakest model. |

### Text Summarization – Model Comparison
| Model                | Semantic F1 | Compression Ratio | Summary Quality |
|----------------------|---------------|----------------------|-----------------|
| **mT5 (Abstractive)** | **0.77**      | **0.27**             | Best summaries; fluent, concise, human-like. |
| **BERT (Extractive)** | 0.61          | 0.38                 | Good meaning preservation; moderate compression. |
| **TF-IDF (Extractive)** | 0.42          | 0.55                 | Fast but shallow; often fails to reduce redundancy. |
