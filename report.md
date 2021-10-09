
# Riyadh food reviews classfication using sentiment analysis

By:
>   Yazeed Musallam



## Abstract
Many restaurants struggle to find their weaknesses, some of them have good specific food such as burgers and bad french fries taste, hence customers’ reviews are important to improve the restaurant, hence proposing a machine learning model that could identify restaurants’ weaknesses is important.

## Design
The data is scrapped from the Google maps and it represents the reviews of restaurants in Riyadh of 270 restaurant and the goal was to analysis it to answer these three main questions:

> 1) What are the positive/negative reviews? </br>
> 2) From user reviews, how we can enhance our restaurant?


## Data Description:
* Datasets with description: </br>
This project based on the following datasets:

> The first dataset contains food reviews which are scrapped from google maps: https://maps.google.com/maps<br />
> <br />
> The second dataset contains amazon food reviews reviews collected from Kaggle: https://www.kaggle.com/snap/amazon-fine-food-reviews <br />


## Scope of the work
Sample size:

>  Apporx. 270 restaurants with 100k reviews.

> Only riyadh city will be involved in this project.

Description for the scrapped dataset as num of rows, number of features/columns, names of columns with description:

Description of scrapped data: </br>
The dataset represent the reviews of riyadh's restaurants

> Number of features:  4 features/Columns

> Number of rows: Approx.: 100K rows

> Names of columns with description and type:

| Field Name | Description                                                                      |
|-------------|---------------------------------------------------------------------------------|
| Review| User's review                                                         |
| Rate      | Review score out of 5                                           |                                 |
| Date        | Date of the review                                                   |
| Restaurant        | Restaurant name                                                             |

<br />
Description for the amazon food reviews dataset as num of rows, number of features/columns, names of columns with description:

Description of scrapped data: </br>
The dataset represent the reviews of riyadh's restaurants

> Number of features:  7 features/Columns

> Number of rows: Approx.: ~500K rows

> Names of columns with description and type:

| Field Name | Description                                                                      |
|-------------|---------------------------------------------------------------------------------|
| Id| Row ID|
| ProductId      |Unique identifier for the product                                           |                                 |
| UserId        | Unqiue identifier for the user                                                   |
| ProfileName        | Profile name of the user                                                             |
| HelpfulnessNume        | Number of users who found the review helpful                                                             |
| HelpfulnessDenume        | Number of users who indicated whether they found the review helpful or not |
| Score        | User score |


## Algorithms

*Data gathering*:
> 1) Web scrapped the reviews from google maps and Kaggle site.
> 2) helper tools:
> >     1- BeautifulSoup
> >     2- Selenium

*Data cleaning*:
> 1) Deleteing the duplicated data points
> 2) Dealing with outliers using feature engineering (i.e. removing number of words>5)
> 3) Deleting: Special character, HTML tags, stop words, Deconcatenation.

*Data validation*:
> 1) Checking no nulls
> 2) Checking no duplicates


*feature engineering*:
</br>
Features added:
 > 1)  Converting 5 rate scale into positive/negative scale
 > 2) Number of Words
 > 3) Number of unique words
 > 4) Number of characters
 > 5) Number of stopwords
 > 6) Number of punctuations
 > 7) Average length of the words

 Model Training &  Evaluation </br>
Data split:</br>
 >  Training: 65% of Google maps reviews + Kaggle dataset</br>
 >  Validation: 15% of Google maps reviews </br>
 >  Testing: 20% of Google maps reviews </br>

Training workflow:
> 1) EDA, to find anomalies in the data such as duplicates and outliers.
> 2) Feature engineering to enhance the model
> 3) Data split into training, validation and testing, training containing from both datasets . 
> 4) The following models are used: <br>
> 4.1) Naive bayes (Baseline) <br>
> 4.2) Logstic regression <br>
> 4.3) Random forest <br>
> 4.4) XGboost <br>
> 4.4) Decision trees <br>
> 4.5) Bert <br>
> 4.6) Long short-term memory (LSTM)
>The best found was BERT achieving F1-SCORE of 83.

BERT results: </br>
 > Training accuracy : 80%</br>
 > Validation accuracy : 81.3%</br>
 > Testing accuracy : 81.2%</br>
 > F1 Score: 83%</br>
 > ROC-AUC score: 89	</br>

The main technologies and libraries that used are:
> - Python
> - Jupyter Notebook
> - HTML/CSS
> - Flask

Libraries:
> - Pandas
> - pickle
> - BeautifulSoup and selenium
> - OS
> - Matplotlib/Seaborn
> - SQLite/SQLalchemy
> - NumPy
> - Sklearn
> - Tensorflow/keras
> - GoogleTrans
> - WordCloud

Processing tools: 
> Google Colab
> </br>


## Communication
Findings: </br>

![image](https://raw.githubusercontent.com/YazeedMusallam/Riyadh-food-reviews-classification-using-machine-learning/main/images/cf.png)
> The above figure shows the confusion matrix, it indicate a good model.
<br>
<br>

![image](https://raw.githubusercontent.com/YazeedMusallam/Riyadh-food-reviews-classification-using-machine-learning/main/images/roc.png)
> The above ROC-AUC curve, with ROC-AUC score: 0.90.

Slide:
<img width="1103" alt="image" src="https://user-images.githubusercontent.com/88656889/136663758-f814aa82-9aa6-4b8e-beba-7433612ba1bd.png">
</br>
<img width="1103" alt="image" src="https://user-images.githubusercontent.com/88656889/136664269-9c9185a2-83b4-448b-88d6-b3982cbea0a3.png">

