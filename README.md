# Readability and Unfairness in Terms of Service Documents

This project examines the relationship between readability and unfairness in Terms of Service (ToS) clauses and, in the process, develops a new readability metric using a combination of Natural Language Processing techniques to provide a more comprehensive characterization.

A full paper was written on this work, including a deeper explanation into the methodology and a discussion of the results. The abstract can be read in the [Paper Abstract](#paper-abstract) section. Please reach out to ksmcl [at] umich [dot] edu if you'd like to access the full paper and/or discuss this work further!

## Table of Contents
- [Usage](#usage)
- [Data](#data)
- [Results](#results)
- [Paper Abstract](#usage)

## Usage

All source code can be found in analyze.ipynb and can be run on a standard local machine.

⭐ Python 3.9+ recommended

Ran using Python 3.11.5

## Data

All data comes from [corpora aggregated by CLAUDETTE](http://claudette.eui.eu/corpora/index.html), a research project aimed at detecting potentially unfair contractual terms in Consumer Contracts and Privacy Policies through machine learning. 
- **TaggedDocuments_142:** Annotated ToS for 142 companies in XML format. Used in final project.
- **TaggedDocuments_50:** Annotated ToS for 50 companies in XML format.

There is overlap between the two datasets, so it is not recommended to combine them.

## Results

Key findings:
- Point-biserial correlation between new readability metric and unfairness yielded a value of -0.077: Unfair clauses show slightly lower readability scores, meaning slightly more readable (p-value = 0.0271)
- PC1 from Principal Component Analysis explained 39% of the data variance. Strongest loadings on Gunning Fog Index, Flesch Reading Ease, average sentence length, and dependency tree depth
- Linear correlation between new readability and Gunning Fog Index scores: 0.8802

## Paper Abstract

Terms of Service (ToS) documents are legal agreements users accept to use digital platforms, yet most people skip them due to complex language. Complexity can conceal unfair terms and exploit the perception that complicated text is trustworthy, and has been a known tactic in other forms of contracts. This project investigates if, and how, textual complexity correlates with unfairness in ToS clauses. Using linguistic features, traditional readability metrics, and pretrained language models, this work assesses readability in a unique measurement using Principal Component Analysis and analyzes its relationship with labeled unfairness scores. The results show a very weak yet statistically significant negative correlation between readability and unfairness, indicating unfair terms are slightly more readable than fair terms. However, the very small magnitude of this correlation indicates that there does not seem to be an intentional difference in readability as it relates to clause fairness in this study’s corpus.

Created in Fall 2025 by Kristine McLaughlin (ksmcl [at] umich [dot] edu).