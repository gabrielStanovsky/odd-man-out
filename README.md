<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Spot the Odd-Man-Out](#spot-the-odd-man-out)
  - [Citing](#citing)
  - [Unpacking the dataset](#unpacking-the-dataset)
  - [Data](#data)
    - [Format](#format)
    - [Expert annotation](#expert-annotation)
    - [Crowdsourced data](#crowdsourced-data)
  - [Contact](#contact)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Spot the Odd-Man-Out

This repository contains the data described in our EMNLP 18 paper: 
[Spot the Odd Man Out: Exploring the Associative Power of Lexical Resources](https://www.semanticscholar.org/paper/Spot-the-Odd-Man-Out%3A-Exploring-the-Associative-of-Stanovsky-Hopkins/2f25629bdd7eec8cc87018d4b8f1a398abeb8917)

The goal of an *Odd-Man-Out* puzzle is simple. Given a set of words, like
"cherry, orange, apple, grass, grape", the objective is to identify the word that does not belong
(here, the answer is grass, because it is not a
fruit).

Most of our puzzles ensure that one of the words is a polysemous *distractor*, making the task especially hard for machines, while human annotators tend to pick the correct odd-man-out with good accuracy.

For example, the table below shows a number of puzzles where the odd-man-out appears in **bold**, and the distractor in *italics*. 

| Category         | Puzzle                                    |
|------------------|-------------------------------------------|
| Construction     | **crane**, *pelican*, excavator, hoist, upraise |
| Guitar part      | **fret**, *crying*, inlays, truss rod, neck     |
| Alcoholic drinks | **gin**, *poker*, vodka, tequila, wine          |
| Card games       | **gin**, *vodka*, bridge, canasta, uno          |


## Citing

```
@InProceedings{Stanovsky2016EMNLP,
  author    = {Gabriel Stanovsky and Mark Hopkins},
  title     = {Spot the Odd Man Out: Exploring the Associative Power of Lexical Resources},
  booktitle = {Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing (EMNLP)},
  month     = {November},
  year      = {2018},
  address   = {Brussels, Belgium},
  publisher = {Association for Computational Linguistics}
}
```
## Unpacking the dataset


	tar xvzf data.tar.gz

## Data

### Format

This collection consists of six sets of "odd-man-out" puzzles. Each puzzle is a single line in the following tab-separated value format:

	CATEGORY <tab> ODD-MAN <tab> ANSWER1 <tab> ANSWER2 <tab> ANSWER3 <tab> ANSWER4

### Expert annotation

The files `common1.tsv`, `common2.tsv`, `proper1.tsv`, and `proper2` were all annotated by experts as part of an [AI2 Hackathon](http://ai2-website.s3.amazonaws.com/data/anomia-2014-11-13.zip).

These consist of two collections of "common noun" puzzles, where the answer options are largely common nouns, and
two collections of "proper noun" puzzles, where the answers options are largely proper nouns. Each collection
contains approximately 100 puzzles.

### Crowdsourced data

The complete unfiltered dataset (which we used for training) is available at `crowdsourced_unfiltered.tsv`, and the validated test set is available at `crowdsourced_filtered.tsv`

## Contact

Please email any questions to 
`gabriel.satanovsky` at `gmail`
