# Reviews of Pharmaceutical Drugs: Analysis & Clustering



## Background & Problem Statement

In the United States, it is common for people to take prescription medication, with approximately 48% of its public taking at least 1 pharmaceutical drug (1). While ailments and metrics of success vary, ultimately, it is the patient's perception that may matter the most. In today's world with online reviews available on a myriad of topics, pharmaceutical drugs are no exception. For this study, I used a dataset containing 161,297 reviews of prescription medications to generate findings that may benefit patients. 

To achieve this goal, I used Pandas and Seaborn to conduct EDA, during which I uncovered findings specific to some of the most frequently represented conditions, which were Birth Control, Depression, Pain, Anxiety, and Acne. I then used NLP with Sentiment Analysis to search for most commmon unigrams, bigrams, trigrams, and to draw comparisons regarding sentiment scores. Finally, I used K-means to create clusters that can be used for further analysis, which I evaluated using silhoutte scores. 

References:

1. FastStats - Therapeutic Drug Use. CDC.  https://www.cdc.gov/nchs/fastats/drug-use-therapeutic.htm. (Reviewed Jan. 2023.)
2. Drug Review Dataset. https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29. (2018) 

## Research Question

How can we use analysis and clustering of pharmaceutical reviews to benefit patients?

## Data Description

### Drug.Com Reviews

I downloaded these reviews from this [website](https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29), which describes the reviews as coming from the website Drugs.com. Both train and test sets are available for download. I used only the train set (which I renamed) as it already contained more than 161,000 reviews, and a train-test-split was not needed.

During preliminary analysis and cleaning, I removed the date column and another column which seemed to contain unique review id numbers, as neither were needed. The original TSV and clean CSV file can be found in the data file.

### Code

01_Data_Import_and_Cleaning.ipynb *Data import, preliminary analysis & cleaning.*
02a_EDA_All_Conditions.ipynb  *Statistical information and visualizations using Pandas & Seborn.*
02b_EDA_Pain.ipynb *Statistical information & visualizations using Pandas & Seaborn. NLP with Sentiment Analysis.*
03_Clustering_Evaluation_Conclusion.ipynb *Clustering of reviews in datasets based on rating, useful count, & sentiment scores.*

## Conclusion, Next Steps & Recommendations

