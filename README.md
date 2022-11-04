# Telco Costumer Churn
## Use Case Summary
### Objective Statement
* Get an insight about the influence of gender on customer churn.
* Describe customer satisfaction seen from the length of their contract that affects customer churn.
* Gain knowledge of how important partners influence customer churn
* Gain knowledge of how important the type of InternetService to influence customer churn
* Get an insight about how much influence the Phone Services on customer churn
* Get an insight about how much influence the Online Security on customer churn
* Get an insight about how much influence the Online Backup on customer churn
* Get an insight about how much influence the Device Protection on customer churn
* Get an insight about how much influence the Tech Support on customer churn
* Get an insight about how much influence the StreamingTV on customer churn
* Get an insight about how much influence the Streaming Movie on customer churn
* Get an insight about how much influence the payment method on Customer Churn
* Create machine learning models to predict customers who will churn

### Challenges
* The data have a lot missing value
* There is data that has an inappropriate data type
* The data scale is not all the same

### Methodology / Analytic Technique
* Descriptive analysis
* Graph analysis
* Machine learning model (classification)

### Business Benefit
* Help marketing strategies to improve products or services so that customer churn can be reduced.
* Help find out which aspects need to be developed to reduce customer churn.

### Expected Outcome
* Knowing the influence of gender on customer churn.
* Knowing customer satisfaction seen from the length of their contract that affects customer churn.
* Knowing how important partners influence customer churn.
* Knowing how important the type of InternetService to influence customer churn
* Get to know how much influence the Phone Services on customer churn.
* Get to know how much influence the Online Security on customer churn.
* Get to know how much influence the Online Backup on customer churn.
* Get to know how much influence the Device Protection on customer churn.
* Get to know how much influence the Tech Support on customer churn.
* Get to know how much influence the StreamingTV on customer churn.
* Get to know how much influence the Streaming Movie on customer churn.
* Gain an insight about how services affect the customer churn.
* Get to know how much influence the payment method on Customer Churn
* Making machine learning models to predict customers who will churn

## Business Understanding
**Customer Churn** refers to the loss of customers. Churn is intimately connected to a company’s performance. The more one learns about buyers’ behavior, the more money one can make. Analyzing customer churn also aids in finding and improving the shortcomings of services provided by the company. Customer churn rate must to be reduce so that the company's income increases

this case has some business question using the data:
* How gender affects the customer churn ?
* How customer satisfaction seen from the length of their contract that affect customer churn ?
* How important partners influences customer churn ?
* How important the type of InternetService to influence customer churn ?
* how many percentage is predict to be churn?

## Data Understanding
### Source Data
* Source Data: [Telco Data](https://github.com/Yesaya03/Machine-Learning-Regression-and-Timeseries/blob/main/data_telco.csv)
* 7043 rows
* 21 columns

### Data Dictionary
Services that each customer has signed
* OnlineSecurity: customer has online security or not (Yes, No, No internet service)
* OnlineBackup: customer has online backup or not (Yes, No, No internet service)
* PhoneService: customer has a phone service or not (Yes, No)
* MultipleLines: customer has multiple lines or not (Yes, No, No phone service)
* InternetService: Customer’s internet service provider (DSL, Fiber optic, No)
* DeviceProtection: customer has device protection or not (Yes, No, No internet service)
* TechSupport: customer has tech support or not (Yes, No, No internet service)
* StreamingTV:customer has streaming TV or not (Yes, No, No internet service)
* StreamingMovies: customer has streaming movies or not (Yes, No, No internet service)

Information account for customer
* tenure : Number of months the customer has stayed with the company
* Contract: The contract term of the customer (Month-to-month, One year, Two year)
* PaymentMethod: The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))
* PaperlessBilling: customer has paperless billing or not (Yes, No)
* MonthlyCharges: The amount charged to the customer monthly
* TotalCharges: The total amount charged to the customer

Demographic info
* gender : male or a female (Male, Female)
* Partner : customer has a partner or not (Yes, No)
* Dependents : customer has dependents or not (Yes, No)
* customerID : Customer ID
* SeniorCitizen :customer is a senior citizen or not (1, 0)

labels for classification
* Churn :customer churned or not (Yes or No)

## Data Preparation
* Python version : 3.9.12
* Packages Version : Pandas, numpy, matplotlib, seaborn, and sklearn

## Data Cleansing
1. There are 13 columns containing missing values, with 12 of them being categorical data so that it is imputed with "unknown" and the remaining 1 column is numeric data with positive-skew distribution so that it is imputed using the median.
2. There is 1 column that has an inappropriate data type so it is necessary to adjust the data type.
3. There are 16 categorical columns that need to be encoded, with 15 of them being nominal data so that they are encoded using One Hot Encoding and the remaining 1 column is ordinal data so that they are encoded using a map.
4. The numeric columns in the dataset have different scales so it is necessary to scale the data using the StandardScaler.
5. The identifier column (customerID) and the multicollinear column (TotalCharges) are removed.

## EDA
### Churn Rate
![image](https://user-images.githubusercontent.com/55911060/200087624-eb562607-a5e1-495b-bd05-91bb221e1786.png)
The graph above shows that most of the customers don't churn, the loyal customer is more than churn customer

### Customer churn Based On Gender
![image](https://user-images.githubusercontent.com/55911060/200087699-985935e1-1ef0-41f8-af9f-c9ceb49bc90c.png)
Based on gender, telco customer distribution seems equal between males and female
The churn rate is almost at an equal level, in other words, we can say that churn rates are not depending on the gender of the customer
from 7043 customers there are 5147 customers who remain subscribed, or about 73.46% of telco data. and based on the results of EDA gender does not have much effect on customer churn, because the percentage results show the same thing, which is in the range of 31% of the total

## CUSTOMER CHURN BASED ON CONTRACT
![image](https://user-images.githubusercontent.com/55911060/200087774-46d16aa9-2656-47d3-828e-ecbd4d71ad31.png)
* Only less than 4% of customers churn when they subscribe for 1 year and 2 years, and this explains that there is no fatal cause that makes customers churn.
* There is an increase in the percentage of about 4.82% between 1-year to 2-year subscriptions for customers who do not churn. that means some loyal customers are still satisfied with the services provided by the company.
* The high number of Month to Month customers who decide to churn is around 23.50%, which means that there are still many early customers who are not interested in the services provided by the company.
