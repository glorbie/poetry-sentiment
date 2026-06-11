# Data Dictionary

## A reference key for the 616-poem sample of modern Korean poetry.


### `seg_id`

- **Type:** integer
- **Description:** Numeric between 1 and 616 identifying a part of a work. No repeats.


### `poem_id`

- **Type:** integer
- **Description:** Numeric between 1 and 483 identifying a whole work. In the case of a poem exceeding a certain length, one poem_id is broken into multiple seg_id


### `text`

- **Type:** string (Korean, NFC-normalized)
- **Description:** The cleaned poem body. Original line breaks have been
  collapsed to spaces (so the text is a single line per row, suitable for
  Orange's File widget). No truncation.

### `title`

- **Type:** string (Korean)
- **Description:** Poem title.
  
### `poet`

- **Type:** categorical (Korean)
- **Description:** Poet name. One of five influential modern Korean poets
  

### `nativeODM_sentiment`

- **Type:** numeric
- **Description:** Sentiment score calculated using Orange Data Mining's native multilingual sentiment dictionary.

### `KNU_sentiment`

- **Type:** numeric
- **Description:** Sentiment score calculated using Kunsan National University's sentiment dictionary.


---

## Used beginning with kpoem_poems_lexicon_sentiment.tsv


### `sen_score`

- **Type:** numeric
- **Description:** Sentiment score calculated by one of the two sentiment dictionaries. Replaces 'nativeODM_sentiment' and 'KNU_sentiment' labels. Pairs with label 'dictionary'

### `dictionary`

- **Type:** categorical
- **Description:** Indicates which dictionary the particular sen_score is associated with


### `average_all_annotators`

- **Type:** numeric
- **Description:** Average sentiment score calculated based on human annotations
