\## 📚 Amazon Kindle Book Reviews Sentiment Analysis (NLP \& ML)



\## 📌 Project Overview

This project focuses on performing \*\*Sentiment Analysis\*\* on Amazon Kindle Store book reviews using Natural Language Processing (NLP) and Machine Learning techniques. By analyzing customer review text (`reviewText`) and product ratings (`rating`), the model classifies reviews into \*\*Positive\*\* or \*\*Negative\*\* sentiments, helping understand reader feedback and automate review classification.



\## 🎯 Project Objectives

\- Clean and preprocess raw text reviews using NLP techniques (lowercasing, regex cleaning, stopword removal, HTML/URL stripping, and lemmatization).

\- Transform numerical star ratings (1–5) into binary sentiment labels (`0 = Negative`, `1 = Positive`).

\- Convert cleaned text data into numerical feature vectors using \*\*Bag of Words (BoW)\*\* and \*\*TF-IDF\*\*.

\- Train and compare \*\*Gaussian Naive Bayes\*\* classifiers on both BoW and TF-IDF representations.

\- Evaluate model performance using Accuracy Score and Confusion Matrix.



\## 🛠️ Technologies \& Libraries Used

\- Python

\- Pandas

\- NLTK (Natural Language Toolkit)

\- BeautifulSoup4 (`bs4`)

\- Regular Expressions (`re`)

\- Scikit-Learn

\- Jupyter Notebook



\## 📂 Dataset Information

The dataset (`all\_kindle\_review.csv`) is a subset of the Amazon Kindle Store 5-core product reviews dataset containing \*\*12,000 records\*\* and \*\*11 columns\*\*, from which the primary columns used for modeling are:

\- \*\*`reviewText`:\*\* Detailed text of the customer's book review.

\- \*\*`rating`:\*\* Star rating of the product (1 to 5), converted into binary classes:

&#x20; - `0` (Negative Sentiment): Rating < 3 (4,000 reviews)

&#x20; - `1` (Positive Sentiment): Rating ≥ 3 (8,000 reviews)



\*(Other metadata columns in the raw dataset include `asin`, `helpful`, `reviewTime`, `reviewerID`, `reviewerName`, `summary`, and `unixReviewTime`.)\*



\## 🧹 Text Preprocessing \& Feature Engineering

1\. \*\*Target Binarization:\*\* Mapped ratings `1` and `2` to `0` (Negative), and ratings `3`, `4`, and `5` to `1` (Positive).

2\. \*\*Text Cleaning:\*\*

&#x20;  - Converted all review text to lowercase.

&#x20;  - Removed special characters and punctuation using Regular Expressions (`re`).

&#x20;  - Removed English stopwords using `nltk.corpus.stopwords`.

&#x20;  - Stripped URLs and HTML tags using `re` and `BeautifulSoup`.

&#x20;  - Normalized extra whitespaces.

3\. \*\*Lemmatization:\*\* Reduced words to their base/dictionary root form using `WordNetLemmatizer`.

4\. \*\*Vectorization (Feature Extraction):\*\*

&#x20;  - \*\*Bag of Words (BoW):\*\* Extracted word frequency vectors using `CountVectorizer` (35,757 unique features).

&#x20;  - \*\*TF-IDF:\*\* Extracted weighted term frequency-inverse document frequency vectors using `TfidfVectorizer`.



\## 🤖 Model Training \& Evaluation

The dataset was split into \*\*80% Training (9,600 reviews)\*\* and \*\*20% Testing (2,400 reviews)\*\* sets, and evaluated using \*\*Gaussian Naive Bayes (`GaussianNB`)\*\*:



| Feature Extraction Technique | Algorithm | Evaluation Metrics |

| :--- | :--- | :--- |

| \*\*Bag of Words (CountVectorizer)\*\* | Gaussian Naive Bayes | Accuracy Score \& Confusion Matrix |

| \*\*TF-IDF (TfidfVectorizer)\*\* | Gaussian Naive Bayes | Accuracy Score \& Confusion Matrix |



\*(Note: Run the final model cells in the notebook to view the exact Accuracy Scores and Confusion Matrices for both vectorizers.)\*



\## ⚙️ How to Run This Project

1\. Install Python and Jupyter Notebook.

2\. Install the required libraries:

&#x20;  ```bash

&#x20;  pip install pandas nltk beautifulsoup4 lxml scikit-learn





\## 📁 Project Structure



Kindle-Review-Sentiment-Analysis/

│

├── Kindle\_Review\_Sentiment\_Analysis.ipynb

├── all\_kindle\_review.csv

└── README.md





Email:sakshikachare444@gmail.com



GitHub: https://github.com/Sakshi-Kachare







\---





⭐ This project demonstrates an end-to-end NLP \& Machine Learning pipeline including Text Cleaning, Lemmatization, BoW/TF-IDF Vectorization, and Sentiment Classification.



