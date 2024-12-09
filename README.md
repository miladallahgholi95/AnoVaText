# AnoVaText: ANOVA Analysis on Text Word Frequencies

## Overview

**AnoVaText** is a Python class that performs ANOVA (Analysis of Variance) to identify important words in a collection of texts based on their frequency differences across different categories (labels). This class leverages the `f_oneway` function from the `scipy.stats` library to perform the F-test on word frequencies between different text groups (corresponding to different labels).

The main goal is to identify which words are significantly associated with different categories based on their frequency distribution across the provided texts.

## Features

- Extracts unique words from a collection of texts.
- Computes word frequencies for each text.
- Performs ANOVA (F-test) to identify words whose frequencies significantly differ between texts of different labels.
- Returns a list of the most important words for each label, based on the F-statistic.

## Requirements

- **numpy**: For numerical computations.
- **scipy**: For statistical functions (e.g., ANOVA test).
- **collections**: For counting word occurrences in each text.

## Usage

### Initialization
To initialize the AnoVaText class, you need to provide the following parameters:

texts: A list of text documents (strings).
labels: A list of labels corresponding to each text (e.g., class or category of the text).
num_important_words: The number of important words to extract for each label based on the ANOVA test.

### Example

```
from AnoVaText import AnoVaText

# Sample texts and labels
texts = ["This is a sample text.", "Another sample text for testing.", "Yet another example."]
labels = ["Category1", "Category2", "Category1"]

# Create an AnoVaText object with the number of important words set to 3
anova_text = AnoVaText(texts, labels, num_important_words=10)
important_words = anova_text.analyze()
```


