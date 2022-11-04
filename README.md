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
