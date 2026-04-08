# 🗣️ Natural Language Processing (NLP) Techniques in Python
## Name: Harshit
## Branch: EnTC A3
## PRN: 25070123053
## 📄 Experiment Title
Text Preprocessing and Feature Extraction using NLP in Python
## 🎯 Objective
The objective of this experiment is to understand the fundamental pipeline of **Natural Language Processing**, focusing on cleaning raw text data and converting it into numerical vectors that machine learning models can interpret.
## 📌 Overview
Human language is messy, unstructured, and filled with noise (punctuation, slang, stop words). NLP techniques allow us to:
 * **Clean** text by removing irrelevant characters.
 * **Standardize** words to their root forms.
 * **Vectorize** text to perform mathematical operations.
These steps are the backbone of sentiment analysis, chatbots, and language translation.
## 🧠 Key Concepts
 * Tokenization & Stop Word Removal
 * Stemming vs. Lemmatization
 * Part-of-Speech (POS) Tagging
 * Bag of Words (BoW)
 * TF-IDF (Term Frequency-Inverse Document Frequency)
 * Word Embeddings
## 📘 Theory
### 🔹 Text Cleaning & Standardization
Before analysis, text must be simplified so the computer recognizes "Running" and "run" as the same concept.
#### 1. Tokenization
Breaking a sentence into individual words (tokens).
> **Input:** "Python is fun." → **Output:** ['Python', 'is', 'fun']
> 
#### 2. Stemming
Cutting off prefixes or suffixes to find the common root (often results in non-words).
 * *Example:* "Studying" → "Studi"
#### 3. Lemmatization
Reducing words to their dictionary base form (Lemma) using vocabulary and morphological analysis.
 * *Example:* "Better" → "Good"
### 🔹 Feature Extraction (Vectorization)
Machine learning models cannot read text; they read numbers.
#### 1. Bag of Words (BoW)
Counts the frequency of each word in a document. It ignores grammar and word order.
#### 2. TF-IDF
Weights words based on how unique they are to a specific document compared to a whole collection (corpus).

#### 3. Word Embeddings (Word2Vec)
Maps words into high-dimensional space where words with similar meanings are mathematically "close" to each other.
### 🔹 Comparison: Stemming vs. Lemmatization
| Feature | Stemming | Lemmatization |
|---|---|---|
| **Speed** | Very Fast | Slower (Linguistic analysis) |
| **Accuracy** | Lower (Crude chopping) | Higher (Context-aware) |
| **Output** | May not be a real word | Always a valid word |
| **Use Case** | Search engines, SEO | Sentiment Analysis, Chatbots |
## ⚙️ Procedure
 1. Install and import libraries (NLTK, Spacy, Scikit-learn).
 2. Download necessary corpora (e.g., stopwords, punkt).
 3. **Clean Text:** Convert to lowercase and remove special characters.
 4. **Tokenize:** Split text into units.
 5. **Normalize:** Apply Stemming or Lemmatization.
 6. **Vectorize:** Convert the cleaned tokens into a TF-IDF or BoW matrix.
## 📘 Implementation
### Basic Cleaning with NLTK
```python
import nltk
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer

# Remove Stopwords
stop_words = set(stopwords.words('english'))
filtered_text = [w for w in tokens if w not in stop_words]

# Lemmatization
lemmatizer = WordNetLemmatizer()
root_word = lemmatizer.lemmatize("running", pos="v")

```
### Vectorization with Scikit-learn
```python
from sklearn.feature_extraction.text import TfidfVectorizer

vectorizer = TfidfVectorizer()
tfidf_matrix = vectorizer.fit_transform(corpus)

```
## 📋 Key Functions
| Operation | Library/Function | Purpose |
|---|---|---|
| **Tokenization** | word_tokenize() | Split sentences into words |
| **Stopwords** | stopwords.words('english') | Filter out "the", "is", "at", etc. |
| **Stemming** | PorterStemmer() | Fast, heuristic root finding |
| **Vectorizing** | CountVectorizer() | Create a Bag of Words matrix |
| **NER** | spacy.load('en_core_web_sm') | Identify Names, Dates, Locations |
## 📂 Applications
 * **Spam Detection:** Filtering "junk" emails based on word patterns.
 * **Sentiment Analysis:** Determining if a review is positive or negative.
 * **Auto-Correction:** Suggesting words based on root similarity.
## 📌 Conclusion
NLP techniques bridge the gap between human communication and machine understanding. By applying cleaning, lemmatization, and vectorization, we transform raw, chaotic text into structured data ready for predictive modeling.
## ✨ Thank You

