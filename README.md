# Domain Generation Algorithm (DGA) Dataset
This repository contains the dataset used in the research paper by T. Wang, L. Chen, & Y. Genc (2021), titled "A Dictionary-Based Method for Detecting Machine-Generated Domains", published in the Information Security Journal: A Global Perspective, Volume 30, Issue 4, pages 205-218. DOI: 10.1080/19393555.2020.1834650.

## Overview
The dataset comprises a total of 100,033 domain names, balanced between 50,033 positive cases (machine-generated domains) and 50,000 negative cases (legitimate domains). This dataset is designed to facilitate the development and evaluation of machine learning models for distinguishing between machine-generated and legitimate domain names.

## Dataset Features
Each entry in the dataset is characterized by the following features:
- `domain`: The domain names.
- `class`: Class label (Positive cases are DGA domains, Negative cases are legit domains).
- `length`: Length of the domain names.
- `entropy`: Entropy of the domain names.
- `KL_unigram`: KL divergence based on the unigram model of domain names.
- `KL_bigram`: KL divergence based on the bigram model of domain names.
- `alexa_bigram_JI`: Bigram Jaccard Index in comparison to Alexa.
- `alexa_Ngrams`: N-gram features based on Alexa data.
- `word_Ngrams`: Proposed N-gram-based dictionary features.

## Data Usage
The dataset is stored in a compressed .gz file format. It can be easily loaded into a pandas DataFrame using the following Python code:
```
import pandas as pd
df = pd.read_csv('domains_features.gz', compression = 'gzip', encoding='utf-8')
```

## Reference
If you found the dataset useful in your research or applications, please cite using the following BibTeX:
```
@article{doi:10.1080/19393555.2020.1834650,
author = {Tianyu Wang, Li-Chiou Chen and Yegin Genc},
title = {A dictionary-based method for detecting machine-generated domains},
journal = {Information Security Journal: A Global Perspective},
volume = {30},
number = {4},
pages = {205-218},
year = {2021},
publisher = {Taylor & Francis},
doi = {10.1080/19393555.2020.1834650},
}
```