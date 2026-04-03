# nlp-learning
NLP basics using Jupyter Notebook
# NLP Practice Notes (Jupyter Notebook)

##  Purpose

This notebook contains my practice on basic NLP (Natural Language Processing) concepts.
It is meant for revision so that I can quickly recall what I learned and how I implemented it.

##  Topics Covered

### 🔹 1. Tokenization

* Broke text into smaller parts:

  * Sentences → `sent_tokenize()`
  * Words → `word_tokenize()`
* Used:

  ```python
  from nltk.tokenize import sent_tokenize, word_tokenize
  ```
* Learned:

  * Text needs to be split before processing
  * Sentence vs word tokenization difference

---

### 🔹 2. Stemming

Reduced words to root form (not always meaningful words)

#### ✔ Porter Stemmer

```python
from nltk.stem import PorterStemmer
```

* Example: *running → run*

#### ✔ Regexp Stemmer

```python
from nltk.stem import RegexpStemmer
```

* Removes patterns using regex

#### ✔ Snowball Stemmer

```python
from nltk.stem import SnowballStemmer
```

* Better version of Porter
* Supports multiple languages

Learned:

* Stemming is fast but not always accurate


### 🔹 3. Lemmatization

```python
from nltk.stem import WordNetLemmatizer
```

* Converts words to meaningful base form
* Example: *better → good*

 Learned:

* More accurate than stemming
* Needs dictionary (WordNet)


### 🔹 4. Stopwords Removal

```python
from nltk.corpus import stopwords
```

* Removed common words:

  * "the", "is", "and", etc.

 Learned:

* Helps reduce noise in text
* Improves model performance


### 🔹 5. Parts of Speech (POS Tagging)

```python
import nltk
nltk.pos_tag(words)
```

* Identified grammar roles:

  * Noun, Verb, Adjective, etc.

 Learned:

* Helps understand sentence structure

---

### 🔹 6. Named Entity Recognition (NER)

```python
nltk.ne_chunk(pos_tags)
```

* Identified:

  * Person names
  * Locations
  * Organizations

 Learned:

* Useful for extracting real-world entities


### 🔹 7. Pretrained Model (spaCy)

```python
import spacy
nlp = spacy.load("en_core_web_sm")
```

* Processed text using spaCy
* Extracted:

  * Tokens
  * POS tags
  * Entities

 Learned:

* spaCy is faster and more advanced than NLTK

## 🔁 My Learning Flow

1. Started with raw text
2. Applied tokenization
3. Cleaned text using stopwords
4. Reduced words using stemming/lemmatization
5. Analyzed grammar using POS
6. Extracted entities using NER
7. Used pretrained model (spaCy)

##  Key Takeaways

* Text preprocessing is the first step in NLP
* Stemming vs Lemmatization difference is important
* Stopwords removal improves efficiency
* POS + NER helps understand meaning
* spaCy is more practical for real-world projects

##  Next Steps (for future me)

* Build Resume Analyzer using NLP
* Try TF-IDF / Bag of Words
* Learn basic ML models for text classification
* Explore sentiment analysis

⭐ This notebook represents my foundational understanding of NLP concepts.
