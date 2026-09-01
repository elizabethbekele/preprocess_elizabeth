# Text Preprocessing Text Python Package

#### Course Link: [Introduction to NLP](https://bit.ly/intro_nlp)

This Python package is created by [KGPTalkie](https://youtube.com/kgptalkie). It provides various text preprocessing utilities for natural language processing (NLP) tasks.

### Installation from PyPi 

You can install this package using pip as follows:

```
pip install preprocessing_elizabeth

```
### Installation from GitHub

You can install this package from GitHub as follows:

```
pip install git+https://github.com/elizabethbekele/preprocess_elizabeth.git

```

### Requirements

You need to install these Python Packages:
```
pip install spacy == 3.8.14
python -m spacy download en_core_web_sm == 3.7.1
pip install nltk == 3.10.0
pip install beautifulsoup4 == 4.13.4
pip install textblob == 0.18.0.post0

```

### Download NLTK Data
If you are using this package for the first time, you need to download NLTK data as follows
```
import preprocess_elizabeth as pe
pe.download_nltk_data()

```
## How to Use the Package

### 1. Basic Text Preprocessing

#### Lowercasing Text

```python
import preprocess_elizabeth as pe

text = "HELLO WORLD!"
processed_text = pe.to_lower_case(text)
print(processed_text)  # Output: hello world!
```

#### Expanding Contractions

```python
import preprocess_elizabeth as pe

text = "I'm learning NLP."
processed_text = pe.contraction_to_expansion(text)
print(processed_text)  # Output: I am learning NLP.
```

#### Removing Emails

```python
import preprocess_elizabeth as pe

text = "Contact me at example@example.com"
processed_text = pe.remove_emails(text)
print(processed_text)  # Output: Contact me at 
```

#### Removing URLs

```python
import preprocess_elizabeth as pe

text = "Check out https://example.com"
processed_text = pe.remove_urls(text)
print(processed_text)  # Output: Check out
```

#### Removing HTML Tags

```python
import preprocess_elizabeth as pe

text = "<p>Hello World!</p>"
processed_text = pe.remove_html_tags(text)
print(processed_text)  # Output: Hello World!
```

#### Removing Special Characters

```python
import preprocess_elizabeth as pe

text = "Hello @World! #NLP"
processed_text = pe.remove_special_chars(text)
print(processed_text)  # Output: Hello World NLP
```

### 2. Advanced Text Processing

#### Lemmatization

```python
import preprocess_elizabeth as pe

text = "running runs"
processed_text = pe.lemmatize(text)
print(processed_text)  # Output: run run
```

#### Sentiment Analysis

```python
import preprocess_elizabeth as pe

text = "I love programming!"
sentiment = pe.sentiment_analysis(text)
print(sentiment)  # Output: Sentiment(polarity=0.5, subjectivity=0.6)
```

#### Detecting and Translating Language

```python
import preprocess_elizabeth as pe
from googletrans import Translator

translator = Translator()
text = "Bonjour tout le monde"
lang = pe.detect_language(text, translator)
translated_text = pe.translate(text, 'en', translator)
print(f"Language: {lang}, Translated: {translated_text}")
# Output: Language: fr, Translated: Hello everyone
```

### 3. Feature Extraction

#### Word Count

```python
import preprocess_elizabeth as pe

text = "I love NLP."
count = ps.word_count(text)
print(count)  # Output: 3
```

#### Character Count

```python
import preprocess_elizabeth as pe

text = "I love NLP."
count = pe.char_count(text)
print(count)  # Output: 9
```

#### N-Grams

```python
import preprocess_elizabeth as pe

text = "I love NLP"
ngrams = pe.n_grams(text, n=2)
print(ngrams)  # Output: [('I', 'love'), ('love', 'NLP')]
```

### 4. Full Example: Cleaning Text

Here’s an example of how you might use several functions together to clean text data:

```python
import preprocess_elizabeth as pe

text = "I'm loving this NLP tutorial! Contact me at udemy@kgptalkie.com. Visit https://kgptalkie.com."
cleaned_text = pe.clean_text(text)
print(cleaned_text)
# Output: i am loving this nlp tutorial contact me at visit
```

### One Short Feature Extraction
```python
import preprocess_elizabeth as pe

pe.extract_features("I love NLP")
```

## Notes

- Be cautious when using heavy operations like `lemmatize` and `spelling_correction` on very large datasets, as they can be time-consuming.
- The package supports custom cleaning and preprocessing pipelines by using these modular functions together.
