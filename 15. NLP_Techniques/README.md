

---

# 🗣️ Experiment 15: Natural Language Processing (NLP) Techniques
**Name:** Harshit  
**PRN:** 25070123053  
**Batch:** A3  
**Branch:** EnTC  

---

## 🎯 Project Objective
The goal of this experiment is to implement and understand the fundamental pipeline of **Natural Language Processing** using Python's **NLTK** library. We focus on transforming unstructured "human" text into a structured format that machines can process through cleaning, normalization, and statistical analysis.


---

## 🧠 Key Concepts & Theory

### 1. Tokenization
The process of breaking down a stream of text into smaller units called **tokens**. 
* **Word Tokenization:** Splitting sentences into individual words.
* **Sentence Tokenization:** Splitting paragraphs into individual sentences.

### 2. Stop Word Removal
Removing commonly used words (e.g., "the", "is", "in") that carry very little unique information. This reduces the "noise" in the dataset and focuses on the keywords.

### 3. Stemming vs. Lemmatization
Both techniques aim to reach the "root" of a word, but they differ in complexity:
* **Stemming (PorterStemmer):** A crude heuristic process that chops off the ends of words. It is fast but often results in non-words (e.g., "studies" becomes "studi").
* **Lemmatization (WordNetLemmatizer):** Uses a dictionary (vocabulary) and morphological analysis to return the word to its base form, known as a **Lemma**.

| Feature | Stemming | Lemmatization |
| :--- | :--- | :--- |
| **Method** | Rule-based "chopping" | Dictionary-based lookup |
| **Speed** | Very Fast | Slower (requires context) |
| **Output** | May not be a real word | Always a valid dictionary word |
| **Accuracy** | Lower | Higher |

### 4. Part-of-Speech (POS) Tagging
The process of marking up a word in a text as corresponding to a particular part of speech based on both its definition and its context.

---

## 💻 Implementation Highlights

### Environment Setup
To run these techniques, specific NLTK datasets must be downloaded:
```python
import nltk
nltk.download('punkt')        # For tokenization
nltk.download('stopwords')    # For stop word lists
nltk.download('wordnet')      # For lemmatization
nltk.download('averaged_perceptron_tagger') # For POS Tagging
```

### Word Normalization Example
Based on our experiment, the difference in output is clear:
* **Stemming `["studies", "coding"]`** $\rightarrow$ `['studi', 'code']`
* **Lemmatization `"studies"`** $\rightarrow$ `'study'`

### Frequency Distribution
We utilize `FreqDist` to calculate the occurrence of each word. For the text *"Python is easy. It is widely used in data science."*, the distribution reveals:
* `'is'`: 2 occurrences
* `'Python'`: 1 occurrence

---

## 🏷️ Comprehensive POS Tag Reference
During the POS Tagging phase, the model assigns specific labels to words. Below is the complete reference table used in this experiment:

| Tag | Description | Example |
| :--- | :--- | :--- |
| **NNP** | Proper noun, singular | London, Microsoft |
| **NN** | Noun, singular or mass | bicycle, air |
| **NNS** | Noun, plural | bicycles, mountains |
| **VBZ** | Verb, 3rd person singular present | writes, takes |
| **VBP** | Verb, non-3rd person singular present | write, take |
| **VBD** | Verb, past tense | wrote, took |
| **VBG** | Verb, gerund or present participle | writing, taking |
| **VBN** | Verb, past participle | written, taken |
| **JJ** | Adjective | green, large |
| **JJR** | Adjective, comparative | greener, larger |
| **JJS** | Adjective, superlative | greenest, largest |
| **RB** | Adverb | quickly, extremely |
| **DT** | Determiner | the, a, an |
| **PRP** | Personal pronoun | I, he, it |
| **PRP$** | Possessive pronoun | my, his, its |
| **IN** | Preposition / Subordinating conjunction | in, of, during |
| **CC** | Coordinating conjunction | and, but, or |
| **CD** | Cardinal number | one, 2026 |
| **MD** | Modal | can, should, will |

---

## 📂 Real-World Applications
* **Sentiment Analysis:** Using POS tagging and Lemmatization to determine if a product review is "Good" or "Bad".
* **Chatbots:** Tokenizing user input to understand intent.
* **Spam Filters:** Using word frequency (Bag of Words) to identify common phrases in junk mail.
* **Search Engines:** Using Stemming to ensure a search for "running" also finds results for "run".

## 📌 Conclusion
Through this experiment, we successfully implemented a text preprocessing pipeline. By cleaning the data and using normalization techniques like Lemmatization, we can significantly improve the accuracy of any downstream machine learning model.

---
*Developed for the Python Programming Lab.*
