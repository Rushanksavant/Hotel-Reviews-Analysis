# Methods Used:

### Step-1 Data Cleaning
A lot of location data is missing, sorting the data having null location values and data with non-null location values, also deleting the rows with no review entries
After this, two datas are formed;
- data_non_null_location.csv
- data_null_location.csv

### Step-2 Using BERT pipeline to calculate Sentiment info of cleaned data
Using the "sentiment-analysis" BERT model pipeline imported from ‘transformers’ package created by ‘Hugging face’. This pipeline model was used to make predictions on all the reviews in data_non_null_location.csv and data_null_location.csv, resulting in;
- sentiment_info_non_null_loc.csv
- sentiment_info_null_loc.csv 

### Step-3 Using BERT pipeline to add Emotion info of cleaned data
Using the "zero-shot-classification" BERT model pipeline imported from the ‘transformers’ package created by ‘Hugging face’ to classify reviews based on ["upset", "satisfied", "anger", "happy"] classes. This pipeline model was used to make predictions on all the reviews in sentiment_info_non_null_loc.csv and sentiment_info_null_loc.csv, resulting in;
- emo_sent_info_non_null_loc.csv
- emo_sent_info_null_loc.csv

### Step-4 Analytics using Tableau 
(on emo_sent_info_non_null_loc.csv and emo_sent_info_null_loc.csv)
- #### Analytics on emo_sent_info_non_null_loc.csv:
Tableau Public Dashboard link- https://public.tableau.com/app/profile/irss350/viz/TestDatawithavailableLocation/Dashboard1

- #### Analytics on emo_sent_info_null_loc.csv:
Tableau Public Dashboard link- https://public.tableau.com/app/profile/irss350/viz/TestDatawithoutLocation/Dashboard1



For Insights and Detailed explanation, visit- https://docs.google.com/document/d/1ysjdKVfHSIfAL36s8PzjxARHsnzOpzT2oPRL0Z7iJTU/edit?usp=sharing
