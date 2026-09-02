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
