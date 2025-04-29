# hOUPSh dataset

This directory contains the result of the annotations organized during the hOUPsh workshop of the [French TALN - 2023 conference](https://coria-taln-2023.sciencesconf.org/).  


# Data description

The dataset is contained in `hOUPSh-v1.csv` file. 

## Columns description
- `ID` : (int) the ID of the item
- `SUB_ID` : (int) : the id of the sub item. It is either `1` or `2` given the fact that one item (question) provides two subitems (answers from human or chatgpt). 
- `Question` : (str) : the question that was asked on Quora
- `Answer` : (str) : the answer to the question, can be either provided by a human or by chatGPT
- `Label` : (str) `human` | `chatgpt` : whether the anwser came from a human or chatgpt
- `Annotations` : (str) : the human annotations of the item. Each annotator is identified by an ID, annotators are separated by `|`
    - For example : `annot-4=human` indicates that the annotator (which ID is `annot-4`) marked the answer as `human`
- `Split` : (str) `one-answer` | `two-answers` : wether only one answer or the two answers (human and chatgpt)  were shown to the annotators.
- `Domain` : (str) `programer` | `hardware` : the domain from which the item was drawn.
- `Source` : (str) : URL of the item in Quora if any else `None`
