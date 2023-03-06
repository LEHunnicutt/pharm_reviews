# Reviews of Pharmaceutical Drugs: Analysis & Clustering



## Background & Problem Statement

In the United States, it is common for people to take prescription medication, with approximately 48% of its public taking at least 1 pharmaceutical drug (1). While ailments and metrics of success vary, ultimately, it is the patient's perception that may matter the most. In today's world with online reviews available on a myriad of topics, pharmaceutical drugs are no exception. For this study, I used a dataset containing 161,297 reviews of prescription medications(2) to generate findings that may benefit patients. 

To achieve this goal, I used Pandas and Seaborn to conduct EDA, during which I uncovered findings specific to some of the most frequently represented conditions, which were Birth Control, Depression, Pain, Anxiety, and Acne. I then used NLP with Sentiment Analysis to search for most commmon unigrams, bigrams, trigrams, and to draw comparisons regarding sentiment scores. Finally, I used K-means to create clusters that can be used for further analysis, which I evaluated using silhoutte scores. 

References:

1. FastStats - Therapeutic Drug Use. CDC.  https://www.cdc.gov/nchs/fastats/drug-use-therapeutic.htm. (Reviewed Jan. 2023.)
2. Drug Review Dataset. https://archive.ics.uci.edu/ml/datasets/Drug+Review+Dataset+%28Drugs.com%29. (2018) 

## Research Question

How can we use analysis and clustering of pharmaceutical reviews to benefit patients?

## Data Description

### Drug.Com Reviews

I downloaded these reviews from the drug review dataset noted above, which describes the reviews as coming from the website Drugs.com. Both train and test sets are available for download. I used only the train set (which I renamed) as it already contained more than 161,000 reviews, and a train-test-split was not needed.

During preliminary analysis and cleaning, I removed the date column and another column which seemed to contain unique review id numbers, as neither were needed. I also made the column names lowercase in order to facilitate their use. The original TSV and clean CSV files can be found in the data folder.

### Code

01_Data_Import_and_Cleaning.ipynb - *Data import, preliminary analysis & cleaning.*<br>
02a_EDA_All_Conditions.ipynb - *Statistical information and visualizations using Pandas & Seborn.*<br>
02b_EDA_Pain.ipynb - *Statistical information & visualizations using Pandas & Seaborn. NLP with Sentiment Analysis.*<br>
03_Clustering_Evaluation_Conclusion.ipynb - *Clustering of reviews in datasets based on rating, useful count, & sentiment scores.*

## Conclusion, Recommendations & Next Steps

The findings of this study include information such as most commonly reviewed, highly rated, and lowly rated drugs for each of the most common conditions. Information was also uncovered regarding which reviews patients find most useful, and introductory work on seeking reviews containing information about certain side effects of pain medications including withdrawal, nausea, drowsiness, and suicidal ideation. Additionally, NLP and Sentiment Analysis revealed differences between reviews of some of the pain medications, such as Oxycodone and Tramadol. All K-Means clustering using reviews from the pain dataset, entire dataset, and all subsets engendered silhoutte scores that were above 0. Most frequently, use of the elbow method led to recommendations of 4 groups, with silhoutte scores as high as 0.544. More in-depth study of the sentiments and language within the reviews, and specifics of each of the clusters, could provide valuable information that providers and/or companies could use to assist patients.

In analyzing reviews, and the ways in which people express themselves through text and numerical ratings, there is a world of information that can be discovered. Patient reviews of drugs are certainly important, as they provide firsthand, descriptive accounts of experiences with specific drugs. With the plethora of drugs that can be prescribed and taken, it is best for as much information as possible to be used in order to give patients the best treatment possible. The preliminary information gathered in this study could be used to provide insight into medication options, and expected side effects. Additionally, the useful count informatation could be used to determine what information patients need. I plan to move forward by seeking opportunities to use patient reviews and other data to improve patient outcomes.