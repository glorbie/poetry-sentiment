
## Project Description
Exploring the limitations of Orange Data Mining and Kunsan National University's sentiment dictionaries through analysis on poetry using colonial and post-liberation Korean works


## Research Questions

Is there a significant disparity between the poem sentiment scores calculated by different lexicon-based approaches? 

How do sentiment scores generated through lexicon-based approaches compare to annotations produced by human experts? 

What is the difference between lexicon-based approaches’ ability to replicate human categorization on positive poems compared to on negative poems? 


## Headline Findings

Direct comparison of sentiment scores calculated by Orange Data Mining’s native dictionary and Kunsan National University’s sentiment dictionary illustrates that while there is overlap between them, there are significant instances of dissimilar and even opposite evaluations. Analysis of the ranges and averages of these ratings reveals that the KNU dictionaries tend to produce more negative scores. When overlaid on human annotations, both dictionaries are shown to perform unremarkably at identifying positive poems, while negative poems are categorized correctly by KNU significantly more frequently than ODM.

## Reproduction Instructions
•	Import file, set tags to meta data
•	create corpus widget, keep ‘text’ as feature, ignore rest
•	connect to preprocessing python script for sentiment analysis (keeping nouns, predicates), change minimum token length to 2
•	connect to corpus widget again, selecting preprocessed text
•	use select row widget to get rid of potential undefined figures
•	Split into two sentiment analysis widgets, one using sentiment analysis native to ODM, the other using KNU’s. 
TBC
