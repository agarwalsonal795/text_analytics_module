Project Overview
This repository contains code, data, and documentation for a text analytics assessment focused on climate-related text. The project covers three main tasks:

Classifying climate sentiment using various machine learning and deep learning models.

Identifying topics associated with climate-related risks and opportunities through unsupervised topic modeling.

Performing named entity recognition (NER) on Twitter data using sequence tagging models.

The aim is to provide robust methods and analysis tools for extracting actionable insights from climate-related textual data.

Features
Climate Sentiment Classification: Implements and compares Naïve Bayes, ClimateBERT, and TinyBERT for sentiment analysis.

Topic Modeling: Uses Latent Dirichlet Allocation (LDA) and Top2Vec to discover key themes in climate texts.

Named Entity Recognition: Applies Conditional Random Fields (CRFs) with custom feature engineering for entity extraction from tweets.

Comprehensive Evaluation: Includes detailed performance metrics, error analysis, and visualizations for each task.

Methods
Climate Sentiment Classification
Data Preprocessing: Lowercasing, tokenization, stopword removal, and lemmatization (WordNet).

Models:

Naïve Bayes: Enhanced with text cleaning and hyperparameter tuning.

ClimateBERT NN: Leverages transfer learning for nuanced sentiment classes.

TinyBERT: Provides balanced performance with deep contextual representations.

Evaluation Metrics: Accuracy, macro F1-score, precision, recall, and confusion matrices.

Topic Modeling
LDA: Applied to Bag-of-Words and TF-IDF representations to find interpretable topics.

Top2Vec: Uses document embeddings to group semantically similar texts and extract context-aware topics.

Visualization: Word clouds and bar plots for topic prominence and coherence.

Comparison: Discusses interpretability and limitations of each method.

Named Entity Recognition (NER) on Twitter
Sequence Tagging: Implements CRFs for NER, with both basic and custom feature sets.

Features: Includes word shape, capitalization, POS tags, context, and Twitter-specific markers (mentions, hashtags, URLs).

Data: Uses the Broad Twitter Corpus (BTC) with BIO tagging scheme.

Metrics: Reports token-level accuracy, entity-level precision/recall/F1, and span-level F1 for practical NER evaluation.

Installation
Clone the repository:

bash
git clone https://github.com/your-username/climate-text-analytics.git
cd climate-text-analytics
Install dependencies (see requirements.txt):

bash
pip install -r requirements.txt
Download any required datasets as described in the data/README.md.

Usage
Climate Sentiment Classification:

bash
python sentiment_classification.py --model naive_bayes
python sentiment_classification.py --model climatebert
python sentiment_classification.py --model tinybert
Topic Modeling:

bash
python topic_modeling.py --method lda
python topic_modeling.py --method top2vec
Named Entity Recognition:

bash
python ner_twitter.py --features custom
Refer to each script's help option (-h) for additional parameters.

Results
Sentiment Classification
Model	Accuracy	Macro F1	Notable Strengths	Notable Weaknesses
Naïve Bayes	0.771	0.76	High precision (neutral)	Lower recall (risk class)
ClimateBERT NN	0.741	0.75	Best recall (nuanced)	Lower precision (neutral)
TinyBERT	0.766	0.77	Balanced performance	Confuses risk/opportunity
Topic Modeling
LDA Topics: "energy", "risk", "carbon", "climate", "emissions", "coal", "oil", etc.

Top2Vec Topics: "stakeholders", "renewables", "sustainability", "risk", "liabilities", "compliance", etc.

NER on Twitter
Model	Token Acc.	Macro F1	Span F1 (PER/LOC/ORG)
Basic CRF	0.8857	0.63	-
Custom CRF	0.9364	0.63	0.73 / 0.54 / 0.41
Limitations and Future Work
Sentiment Classification: Struggles with minority classes and overlapping contexts. Future work: data augmentation, ensemble models, domain-specific pretraining.

Topic Modeling: LDA may conflate topics with overlapping vocabulary; Top2Vec sensitive to hyperparameters. Future work: supervised topic models, larger corpora.

NER: Most errors from ambiguous or multi-token entities. Future work: neural sequence taggers, contextual embeddings, data augmentation.
