# Foodalytics: Trusted analysis to improve your restaurant! (MVP):

### Goal the project:

> The goal of this project is to, build a robust user reviews classifcation model.
### Data:
> The chosen data is 270 restaurants with 100k reviews from google maps, more 100k added from Kaggle dataset.

### Training workflow:
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
>The best found was LSTM achieving ROC AUC score of 90.

### Findings:
![image](https://raw.githubusercontent.com/Naif-Albader/Regression_Project/main/images/RealVsPredicted.png)
> The above figure shows predicted target vs real target; the figure shows a slight good model.
<br>
<br>

![image](https://raw.githubusercontent.com/Naif-Albader/Regression_Project/main/images/Sample.png)
> The above a sample of tested data (Area 500, Location: "الياسمين"), the prediction show the value of land after 5 years.
