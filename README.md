# Text Learning
Text Learning | Example code and own notes while taking the course "Intro to Machine Learning" on Udacity.

## Bag of words
> In this model. text (such as a sentence or a document) is represented as the bag (multiset) of it's words, disregarding grammar and even word order but keeping multiplicity. ([Wikipedia](https://en.wikipedia.org/wiki/Bag-of-words_model))

### Count Vectorizer
Give the array of sentences or documents and fit/transform `vectorizer.vocabulary_.get("greet")`

Not all words are equal! Some words contain more information than others!

## Stopwords
You should remove the words called "stopwords" like; the, in, for, you, will, have, be.

### NLT | Natural Language Toolkit
```python
from nltk.corpus import stopwords
sw = stopwords.words("english")
```

## Stemming
In linguistic morphology and information retrieval, stemming is the process of reducing inflected (or sometimes derived) words to their word stem, base or root form—generally a written word form.

For exapmple, the words below:
- unresponsive
- response
- responsivity
- respond

After using stemmer, they all transformed into "respon".

```python
from nltk.stem.snowball import SnowballStemmer
stemmer = SnowballStemmer("english")
stemmer.stem("responsive")
```

## Tf-Idf Representation

**Tf | Term frequency:** like bag of words.
> The weight of a term that occurs in a document is simply proportional to the term frequency.

**Idf | _Inverse_ document frequency:** weighting by how often word occurs in corpus.
> The specificity of a term can be quantified as an inverse function of the number of documents in which it occurs.
