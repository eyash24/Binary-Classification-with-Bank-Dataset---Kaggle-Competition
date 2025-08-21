# Binary Classificatoin with Bank Dataset 
It is a part of the Kaggle Playground Series Season 5 episode 8

## About the original dataset:
Link to original dataset: [Bank Marketing Dataset Full](https://www.kaggle.com/datasets/sushant097/bank-marketing-dataset-full?select=bank-full.csv) \

The dataset contains 45,211 entries with 17 attributes. The attributes represent client information and campaign details, and they include both categorical and numerical data.
- age: Age of the client (numeric)
- job: Type of job (categorical: "admin.", "blue-collar", "entrepreneur", etc.)
- marital: Marital status (categorical: "married", "single", "divorced")
- education: Level of education (categorical: "primary", "secondary", "tertiary", "unknown")
- default: Has credit in default? (categorical: "yes", "no")
- balance: Average yearly balance in euros (numeric)
- housing: Has a housing loan? (categorical: "yes", "no")
- loan: Has a personal loan? (categorical: "yes", "no")
- contact: Type of communication contact (categorical: "unknown", "telephone", "cellular")
- day: Last contact day of the month (numeric, 1-31)
- month: Last contact month of the year (categorical: "jan", "feb", "mar", …, "dec")
- duration: Last contact duration in seconds (numeric)
- campaign: Number of contacts performed during this campaign (numeric)
- pdays: Number of days since the client was last contacted from a previous campaign (numeric; -1 means the client was not previously contacted)
- previous: Number of contacts performed before this campaign (numeric)
- poutcome: Outcome of the previous marketing campaign (categorical: "unknown", "other", "failure", "success")
- y: The target variable, whether the client subscribed to a term deposit (binary: "yes", "no")

## Competition Dataset
The competition dataset is derived from the original and consist of synthetically added data. \
It comprises of 1000000 rows and 17 features. And is split into train and test by the competition organiser itself. \

### Observations about the dataset
- It is an imbalanced dataset. The train dataset consists of 87% of y label 0, or no.
- It consist of "unknown" in few of the features and they seem to be of significance.
- Numerical features seem to be left-skewed. 
- A lot of outliers exists and they have been left untouched (not removed yet).

### Approaches to deal with the issues in the dataset:
1. For the left-skewed, I thought of performing log transformation but have undertaken the approach of using StandardScaler.
2. Outliers are too many and am currently evaluating the model performance without removing them.
3. A few approaches have been dealth with in regards to the imbalance:
    1. Random Sampling: I have performed over and undersampling
    2. SMOTE 
    3. BalancedBaggingClassifier from imblearn

### Models training and evaluating:
- Logistic Regression
- Random Forest
- Gradient Boost 
- AdaBoost
- Decision Tree and it's variants
- K-Nearest Neighbour
- Support Vector Classifier
- Gaussion Naive Bayes
- Bernoulli Naive Bayes
- Multi-layered Perceptron
- XgBoost
- Artificial Neural Network 
