
## Project Description
Exploring the limitations of Orange Data Mining and Kunsan National University's sentiment dictionaries through analysis on poetry using colonial and post-liberation Korean works


## Research Questions

Is there a significant disparity between the poem sentiment scores calculated by different lexicon-based approaches? 

How do sentiment scores generated through lexicon-based approaches compare to annotations produced by human experts? 

What is the difference between lexicon-based approaches’ ability to replicate human categorization on positive poems compared to on negative poems? 


## Headline Findings

Direct comparison of sentiment scores calculated by Orange Data Mining’s native dictionary and Kunsan National University’s sentiment dictionary illustrates that while there is overlap between them, there are significant instances of dissimilar and even opposite evaluations. Analysis of the ranges and averages of these ratings reveals that the KNU dictionaries tend to produce more negative scores. When overlaid on human annotations, both dictionaries are shown to perform unremarkably at identifying positive poems, while negative poems are categorized correctly by KNU significantly more frequently than ODM.




## Step-By-Step Reproduction Instructions
(see annotations on ODM_Workflow.svg for better visualization)

1. import file, set tags to meta data
2. create corpus widget, keep ‘text’ as feature, ignore rest
3. connect to preprocessing python script for sentiment analysis (keeping NNG, NNP, VV, VA, VV-I, VA-I, VV-R, and VA-R), keep minimum token length to 2
4. connect another corpus widget, selecting preprocessed text
5. split pipeline into two sentiment analysis widgets, one using the multilingual dictionary native to ODM, the other using the processed KNU dictionaries as a custom option
6. use edit domain widgets to rename the sentiment numeric categories to prevent later confusion
7. merge the split pipelines back together using the merge data widget
8. connect a data table widget and then create a scatter plot by placing the different dictionaries on either axis = Figure 1
9.  import file kpoem_poems_lexicon_sentiment.tsv
10. attach box plot widget, set variable to sen_score and subgroup by dictionary = Figure 2
11. import file kpoems_poems_with_average.tsv
12. connect distributions widget, set variable to average_all_annotators, set bin width to 0.1 = Figure 3 
13. connect a box plot widget directly to step 11's file, set variable to average_all_annotators = Figure 4
14. import file combined_human_lexicon.tsv, to itconnect a data table widget
15. use the select rows widget to set the parameter of average_all_annotators is greater than 0
16. attach a distributions widget, set variable to sen_score, set bin width to 5, split columns by dictionary = Figure 5
17. *originally repeated step 15 here with negative numbers and then used the data sampler widget to generate a subset of data, but that has since been added to a tsv file of its own:*
18. import file negative_sample_file.tsv
19. attach a distributions widget, set variable to sen_score, set bin width to 5, split columns by dictionary = Figure 6

