# NLP Preprocessing and Text Classification

This project implements a full NLP preprocessing and text classification workflow in Jupyter Notebook.

## Objective
Build a machine learning text classifier and evaluate it using standard metrics.

## Learning Outcomes Covered
- NLP preprocessing: tokenization, stopword removal, stemming, lemmatization
- Text vectorization: CountVectorizer and TF-IDF
- Classification model training and comparison
- Performance evaluation with accuracy, precision, recall, F1, confusion matrix, and ROC-AUC

## Project Files
- `NLP_Preprocessing_and_Text_Classification.ipynb`: Main notebook with all analysis and code.
- `requirements.txt`: Required Python packages.
- `outputs/` (generated after running notebook):
  - `figures/`: saved plots
  - `models/`: trained model and label encoder
  - `*.csv`: comparison tables and analysis outputs
  - `run_metadata.json`: reproducibility metadata
  - `submission_checklist.md`: submission-ready checklist

## Dataset
Default dataset source used in notebook:
- SMS Spam Collection (TSV):
  - https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv

You can also place a local file at `data/sms.tsv` with columns:
- `label`
- `text`

## How to Run
1. Create a virtual environment (recommended).
2. Install dependencies:
   - `pip install -r requirements.txt`
3. Open the notebook and run all cells from top to bottom.
4. Check generated artifacts in the `outputs/` folder.

## Research Paper Reference
Referenced paper in notebook:
- McCallum, A., & Nigam, K. (1998).
  *A Comparison of Event Models for Naive Bayes Text Classification*.
  https://cdn.aaai.org/Workshops/1998/WS-98-05/WS98-05-007.pdf

Notebook includes:
- key paper insights
- mapping of those insights to implementation choices

## Real-World Application Discussion
The notebook includes a trade-off table comparing:
- Naive Bayes
- Logistic Regression
- Linear SVM
- Deep learning approaches
- Transfer learning approaches (BERT-family)

## Submission Checklist
- [x] Code in Jupyter Notebook
- [x] Dataset link provided
- [x] Visualizations included and labeled
- [x] Research paper reference and mapping included
- [x] Model comparison and analysis included
- [ ] GitHub repository link added

GitHub repository link:

