# Phishing Email Detection Model (Thiranex Task 3)

A machine learning model built with Scikit-learn that classifies emails as **Phishing** or **Safe**, and explains the red flags behind each verdict.

## Features
- Trains on a dataset of phishing and legitimate emails
- Combines two kinds of features:
  - **Text features:** TF-IDF (unigrams and bigrams) on the email body
  - **URL and keyword features:** raw IP links, URL shorteners, suspicious domain extensions, HTTP-only links, many subdomains, '@' in URLs, urgency / credential / money words, exclamation marks, uppercase and digit ratios
- Compares Logistic Regression and Random Forest, then keeps the better model
- Displays accuracy, classification report, confusion matrix and 5-fold cross-validation
- `predict_email()` returns the verdict, the phishing probability and a list of red flags
- Trained model can be saved with joblib

## Dataset
Phishing validation emails dataset (2,000 emails labeled *Safe Email* / *Phishing Email*)
Genchev, E., Miltchev, R., Rangelov, D. (2024). Zenodo. DOI: 10.5281/zenodo.13474746
Licence: CC BY 4.0. The notebook downloads it automatically.

## Results
| Metric | Value |
|--------|-------|
| Best model | [ADD YOUR BEST MODEL] |
| Test accuracy | [ADD YOUR ACCURACY]% |
| 5-fold CV accuracy | [ADD YOUR CV ACCURACY]% |

Confusion matrix:

![Confusion Matrix](confusion_matrix.png)

## Sample Predictions
Add screenshots of `predict_email()` output here.

## How to Run
1. Open `Task3_Thiranex.ipynb` in Google Colab.
2. Run the cells in order (code cell first, then the dataset download and training cell).
3. Test your own emails with the prediction cell.

Requirements: Python 3.8+, pandas, numpy, scikit-learn, matplotlib, joblib (all pre-installed in Colab).

## Project Structure
```
Task3_Thiranex.ipynb     # notebook with code, training and predictions
confusion_matrix.png     # evaluation plot
README.md
```

## Limitations
- The dataset is small (2,000 emails), so results can vary between runs and may not generalise to all real-world emails.
- Handcrafted URL features work on links in the email text only; they do not visit or check the live websites.
- Accuracy should be re-checked on a larger dataset before any real-world use.

## Tech Stack
Python, Scikit-learn, Pandas, NumPy, Matplotlib
