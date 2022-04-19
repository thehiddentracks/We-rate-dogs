# We-rate-dogs
"Wrangle and Analyze Data" project for Udacity's "Data Analyst" micro degree

**Introduction to the project**<br>
For this project I wrangle data associated with tweets of Twitter user "dog_rates". The dataset is based on three individual sets being provided by different sources:

A twitter archive dataset containing tweet data directly from the user. This dataset is being provided as a download.

An image prediction dataset containing information about the dog breeds. This dataset is being hosted on a server and should be downloaded programaticallly.

A dataset containing retweet and favorite counts of tweets. This dataset needs to be created based on a request to the Twitter API.

The goal is to wrangle all datasets to create interesting and trustworthy analyses and visualizations.

**Gathering data**<br>
First, I start with importing all needed modules for this project. Next I start gathering all datasets. The twitter archive, available as a CSV, can be downloaded and uploaded into the notebook. The second dataset requires me to create a request for accessing the given url leading to the file on the server. The request I save as a TSV file in the notebook. For the third dataset I requested a developer access for Twitter. I use the provided credentials to access the Twitter API and download the counts for every tweet from the archive dataset and save the JSON content line by line in a TXT file. Then I create a dataframe out of it only containing the columns I am looking for.

**Assessing data**<br>
I visually and programatically assess all three datasets one by one. I am looking at the content and structure given in each table and column and then have a closer look via programatically checking for duplicates, counting values, checking datatypes and the distribution of the data. There are many things that can be fixed and cleaned, but I focus on eight quality and two tidiness issues.

**Cleaning data**<br>
Before starting cleaning the data, I make copies of all three datasets and continue working with the copies. Most of the quality issues in the datasets are based on missing values, wrong content, or wrong formatting. All of issues I fix with the help of various replace, query, and split commands. The tidiness issues I fix in combining and reducing various columns and combining two tables as thir content fits thematically.

**Storing data**<br>
I create a combination of all tables in a master table and drop the not needed columns that appear empty after prevous cleaning steps.

**Analyzing and visualizing data**<br>
For the analyzing part I check the newly created master dataset for findings about the dog breeds and their popularity. I look at the distribution and value count of the breeds as well as the number of dog ratings to define my findings. For the visualization part I plot the number of most occuring dog breeds in the tweets to show which dogs were mentioned the most. Additionally I plot the mean of the favorite count per dog breed to show that despite appearing quite often in the previous chart, the most popular dogs in the tweets are not the most popular dogs according to the audience favorite count.
