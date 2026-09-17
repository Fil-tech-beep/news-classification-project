# news-classification-project
University news classification project exploring text preprocessing, feature engineering, machine learning models, ensembles, and embeddings. This is a project overview; source code is private.

---

A university group project investigating how to classify news articles
into seven categories: International News, Business, Technology,
Entertainment, Sports, General News, and Health.

The project explores how text representations, article metadata, and
different classification methods affect predictive performance.

This repository provides a public overview of the work.
The implementation is maintained in a private team repository.

## My contribution

My work focused on exploratory data analysis, data preparation, and
baseline modelling:

- Investigating missing values, inconsistent formatting, and feature
  distributions.
- Cleaning article text, titles, publisher information, and timestamps.
- Building TF-IDF representations of titles and articles, experimenting
  with separate and combined text features.
- Exploring dimensionality reduction with Truncated SVD and incorporating
  publisher and date features.
- Developing and tuning random-forest baselines, inspecting classification
  reports and confusion matrices, and preparing prediction exports.

## Approach and results

The experiments used article titles and bodies alongside metadata such
as publisher, publication date, and page rank.

We explored:

- Text cleaning, tokenization, lemmatization, and missing-value handling.
- Word and character TF-IDF features, feature hashing, and Truncated SVD.
- Random forests, linear SVMs, logistic regression, SGD classifiers,
  and Naive Bayes.
- Ensembles combining predictions from multiple classifiers.
- Alternative representations using pretrained MiniLM embeddings,
  Word2Vec, and a small embedding-based neural network.
- Exploratory visualizations, including word clouds, dimensionality
  reduction plots, and clustering analysis.

The model-selection notebook compares linear SVM, logistic regression,
and a soft-voting ensemble using five-fold stratified cross-validation
and macro F1.

Its saved comparison reports:

| Model | Mean cross-validation macro F1 |
|---|---:|
| Soft-voting ensemble | 0.7024 |
| Linear SVM | 0.7014 |
| Logistic regression | 0.6660 |

The ensemble combines logistic regression, an SGD classifier, and a
calibrated linear SVM. It achieved the highest recorded score in this
comparison, with a small numerical improvement over the standalone SVM.

These results come from saved notebook outputs for an earlier
three-configuration run; the current search grid has since been expanded.
They are development-set cross-validation results, not independent
test-set scores. Model selection and subsequent reporting reuse the
development data.

The recorded per-class report shows stronger performance on Sports
and Technology, with General News and Entertainment proving more
challenging.

## Team

A collaborative project by Filippo Montecchi and
[frfede](https://github.com/frfede).

## Source code

The implementation is maintained in a
[private repository](https://github.com/frfede/ds-assignment).
Access is restricted to authorized collaborators.
