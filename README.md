*Wrangling report for the tweet archive of Twitter user @dog_rates* <br>

*Introduction* <br>

The dataset for this project was from the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though almost always greater than 10. 11/10, 12/10, 13/10, etc. WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for students to use in this project. My wrangling efforts in this project is categorized into sections:

Gathering data
Assessing data
Cleaning data
Gathering Data
Data was gathered or collected from 3 sources:

I downloaded the WeRateDogs Twitter archive data (twitter_archive_enhanced.csv) directly. The dataset consisted of 2356 rows and 17 columns.
I used the Requests library to download the tweet image prediction file (image_predictions.tsv) programmatically. The URL from which the file was downloaded is https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv. This dataset contained 2075 rows and 12 columns.
I used the Tweepy library to query additional data via the Twitter API (tweet_json.txt). The tweet_id column from the first dataset was used to gather two additional properties of the WeRateDogs Twitter archive data, i.e retweet_count and favorite_count columns in a new dataframe. It consisted of 1774 rows and 3 columns.
Assessing Data
The 3 datasets were assessed or inspected visually and programmatically to check for data quality issues (such as missing values, duplicates, incorrect data, etc) and lack of tidiness or structural issues. Some of the issues detected and documented were as follows:

columns with missing values
wrong datatype
outliers
less descriptive column names
values of columns as column headers, etc
Cleaning Data
I began this section by first making a copy of the original datasets before cleaning the issues identified. Each of the issues identified were defined as a task which would be done. Code was written to perform the cleaning task. The code was tested to ensure the cleaning task was done as expected.

After all the detected issues were defined, coded and tested, the 3 datasets were merged into a master dataset and stored as a CSV file ("twitter_archive_master.csv")
