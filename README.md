🌱 Climate Text Analytics
This repository contains code, data, and documentation for a text analytics project focused on climate-related textual data. The project addresses three key Natural Language Processing (NLP) tasks: Sentiment Classification, Topic Modeling, and Named Entity Recognition (NER).

📌 Project Overview
This assessment explores robust NLP methods to extract actionable insights from climate-related texts, particularly focusing on social media (e.g., Twitter) and domain-specific reports.

Main Tasks:

Climate Sentiment Classification: Classify sentiment in climate texts using ML and deep learning models.

Topic Modeling: Identify key themes and topics around climate risks and opportunities.

Named Entity Recognition (NER): Extract entities from climate-related Twitter data using sequence tagging.

✨ Features
Climate Sentiment Classification

Implements and compares:

Naïve Bayes

ClimateBERT

TinyBERT

Evaluates performance across nuanced sentiment classes.

Topic Modeling

Uses LDA and Top2Vec to uncover major themes in climate text.

Provides interpretability through word clouds and topic visualizations.

Named Entity Recognition (NER)

Applies Conditional Random Fields (CRFs) with:

Custom feature engineering (word shape, POS tags, Twitter markers).

Trained on the Broad Twitter Corpus (BTC).

Comprehensive Evaluation

Includes metrics: Accuracy, Macro F1, Precision, Recall, Confusion Matrices, Span-level F1, and visual error analysis.

🛠️ Methods Summary
Climate Sentiment Classification
Preprocessing: Lowercasing, tokenization, stopword removal, lemmatization.

Models:

Naïve Bayes: With hyperparameter tuning.

ClimateBERT NN: Transfer learning for climate-specific sentiment.

TinyBERT: Compact transformer for contextual sentiment.

Evaluation:
Accuracy | Macro F1 | Precision | Recall | Confusion Matrices

Topic Modeling
LDA: Bag-of-Words and TF-IDF based topic discovery.

Top2Vec: Embedding-based semantic topic grouping.

Visualization: Word clouds and topic frequency plots.

Comparison: Interpretability vs contextual richness.

Named Entity Recognition (NER) on Twitter
Models: CRFs with basic and custom features.

Feature Set: Word shape, capitalization, POS tags, mentions, hashtags, URLs.

Dataset: Broad Twitter Corpus (BTC) with BIO tagging.

Metrics:
Token Accuracy | Entity-level Precision/Recall/F1 | Span-level F1

📈 Results Summary
Task	Model	Accuracy	Macro F1	Key Notes
Sentiment Classification	Naïve Bayes	0.771	0.76	High neutral precision, low risk recall
ClimateBERT NN	0.741	0.75	Best nuanced recall, lower neutral precision
TinyBERT	0.766	0.77	Balanced performance, some class confusion
Topic Modeling	LDA	-	-	Topics: energy, risk, carbon, emissions
Top2Vec	-	-	Topics: stakeholders, renewables, liabilities
NER (Twitter)	Basic CRF	0.8857	0.63	-
Custom CRF	0.9364	0.63	Span F1: PER=0.73, LOC=0.54, ORG=0.41

🚧 Limitations and Future Work
Sentiment Classification:
Struggles with minority classes and overlapping sentiment contexts.
Future Work: Data augmentation, ensemble models, domain-specific pretraining.

Topic Modeling:
LDA may blur topics with shared vocabularies. Top2Vec sensitive to hyperparameters.
Future Work: Supervised topic models, larger datasets.

NER:
Errors from ambiguous and multi-token entities.
Future Work: Neural sequence taggers (e.g., BiLSTM-CRF, transformer-based models), contextual embeddings, data augmentation.

🚀 Installation
bash
Copy
Edit
git clone https://github.com/your-username/climate-text-analytics.git
cd climate-text-analytics
pip install -r requirements.txt
Download required datasets as described in data/README.md.

⚙️ Usage
Climate Sentiment Classification
bash
Copy
Edit
python sentiment_classification.py --model naive_bayes
python sentiment_classification.py --model climatebert
python sentiment_classification.py --model tinybert
Topic Modeling
bash
Copy
Edit
python topic_modeling.py --method lda
python topic_modeling.py --method top2vec
Named Entity Recognition (NER)
bash
Copy
Edit
python ner_twitter.py --features custom
For all scripts, use the -h flag for additional parameters and usage details.
