## These files are edited versions of the source data or existing sentiment dictionaries. They mainly feature small changes that help to act as work-arounds for some of the limitations of Orange Data Mining's graphing capabilities (or my limitations of knowledge about them).


**Processed KNU Dictionaries**

negative_processed.txt and positive_processed.txt are modifications of Kunsan National University (KNU)'s Korean language sentiment analysis dictionaries. They have had -다 (found at the end of Korean infinitive verbs) removed from the line-final positions in order to make it compatable with Kiwi. Imported into Orange Data Mining (ODM)'s Sentiment Analysis widget as custom dictionaries.



**Lexicon-Based Sentiment Score**

kpoem_poems_lexicon_sentiment.tsv combines the sentiment scores calculated with ODM's native multilingual sentiment dictionary with those calculated by KNU. Created to fix the issue of not being able to subgroup the boxplots by different numerical variables.
Within the dataset, each poem is listed TWICE to allow for two different dictionary tags (now metadata) and different cooresponding sentiment scores. Used in Figure 2.



**Human-Annotation-Based Sentiment Scores**

kpoem_poems_with_average.tsv contains novel sentiment scores calculated by assigning numeric values (1, -1, 0) to the expert annotations from the original dataset. The average of the 5 experts' scores is then taken to be used in comparisons with the lexicon-based approaches. Used in Figures 3 and 4.



**Combined Human/Dictionary Lexicon**

combined_human_lexicon.tsv merges the average human-annotated sentiment scores for each poem onto a dataset (kpoem_poems_lexicon_sentiment.tsv) that features both dictionary sentiment scores. Used in Figure 5, sampled by negative_sample_file.tsv



**Negative Sample File**

negative_sample_file.tsv contains a sample of 174 negative poems generated with a randomizer to match smaller dataset of positive poems. Again, each poem is listed twice to allow for two different dictionary tags and different cooresponding sentiment scores. There is likely a cleaner way to do this, but I just needed this to create Figure 6 in the distributions widget.

