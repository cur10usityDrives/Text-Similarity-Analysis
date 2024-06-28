# Text Similarity Analysis with Various Encoding Techniques

## Overview

This project explores text similarity analysis using different encoding techniques and preprocessing steps. 
It aims to evaluate how these factors impact the accuracy of measuring similarity between pairs of sentences.

## Key Components

### 1. Preprocessing

- **Tokenization**: Sentences are tokenized into words using NLTK's `word_tokenize`.
  
- **Stop-word Removal**: Common English stop words (e.g., "the", "is", "and") are removed to focus on meaningful content words.
  
- **Stemming**: Words are stemmed to their root form using the Porter Stemmer algorithm, reducing inflectional forms and variants.

### 2. Encoding Techniques

- **One-Hot Encoding**: Represents each word in the sentence as a binary vector, where each word presence is marked as 1 or 0.
  
- **Bag-of-Words**: Represents each sentence as a vector of word frequencies in a predefined dictionary (vocabulary).
  
- **Term Frequency (TF)**: Represents each word in the sentence as its frequency of occurrence within the sentence.
  
- **Term Frequency-Inverse Document Frequency (TF-IDF)**: Weighs each word by its frequency in the document and inversely by its
                                                          frequency across all documents (sentences).

### 3. Similarity Measurement

The similarity between pairs of sentences is measured using the cosine similarity metric. Cosine similarity computes the cosine 
of the angle between two vectors of word counts (or TF-IDF scores), providing a measure of similarity irrespective of the sentence length.

### 4. Evaluation Scenarios

Several scenarios are evaluated to demonstrate the impact of preprocessing steps (stop-word removal, stemming) 
and encoding techniques on similarity measurement:

- **Stop-word Removal**: Increases recall but may decrease precision.
  
- **Stemming**: Increases recall by reducing word variations but may decrease precision.
  
- **Encoding Techniques**: One-hot encoding, bag-of-words, TF, and TF-IDF are compared for their precision in capturing semantic similarity.

### 5. IDF Calculation

The project includes a calculation of Inverse Document Frequency (IDF) for terms in a given corpus (sentences). IDF is used to 
weight terms by their rarity across the corpus, enhancing the discriminative power of TF-IDF.

## Usage

### Dependencies

- Python 3.x
- NLTK (Natural Language Toolkit)
- scikit-learn (for CountVectorizer and TfidfVectorizer)

Install dependencies using `pip`:

```bash
pip install -r ...
```

### Running the Project

1. Clone the repository.

2. Ensure you have the necessary NLTK corpora downloaded:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

3. Run the script to execute evaluation scenarios.

### Example Output

The script provides detailed output for each scenario, including original similarity scores and scores after preprocessing 
(stop-word removal, stemming) and encoding.

## Conclusion

This project serves as a foundational exploration into text similarity analysis using various preprocessing techniques and 
encoding methods. It highlights the trade-offs between recall and precision and provides insights into optimizing text 
similarity computations for different applications.

## Author

Natnael Haile
