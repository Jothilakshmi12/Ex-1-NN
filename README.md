<H3>ENTER YOUR NAME</H3> Jothilakshmi.P
<H3>ENTER YOUR REGISTER NO.</H3> 212223110017
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>

STEP 2:Importing the dataset<BR>

STEP 3:Taking care of missing data<BR>

STEP 4:Encoding categorical data<BR>

STEP 5:Normalizing the data<BR>

STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```python
#import libraries
from google.colab import files
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

#Read the dataset from drive
df=pd.read_csv('/content/Churn_Modelling.csv')
df

# Finding Missing Values
print(df.isnull().sum())

#Handling Missing values
df.fillna(df.mean(),inplace=True)
print(df.isnull().sum())

y=df.iloc[:,-1].values
print(y)

#Check for Duplicates
df.duplicated()

#Detect Outliers
df.describe()

#Normalize the dataset
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)

#split the dataset into input and output
x=df.iloc[:, :-1].values
print(x)
y=df.iloc[:,-1].values
print(y)

#splitting the data for training & Testing
X_train ,X_test ,y_train,y_test=train_test_split(x,y,test_size=0.2)

#Print the training data and testing data
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```


## OUTPUT:
### dataset:
![op 1](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/0b8e1cf7-85e7-4a2d-8fd2-486a57bec769)
### Finding Missing Values:
![op 2](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/8868a048-2dec-4fee-a350-168b053837e2)
### Handling Missing values:
![op 3](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/99ccfa53-d072-4ba9-a27f-99b213716927)
### Duplicates:
![op 4](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/6c0f56e8-1c3d-4213-87db-6f89bce9ff5b)
### Normalize the dataset:
![op 5](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/205e185b-6b2b-4841-8f7f-a31f88a4e52b)
### split the dataset into input and output:
![op 6](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/578c756d-b28d-4e87-8cd6-420e7c8b38a0)
### splitting the data for training & Testing:
![op 7](https://github.com/Jothilakshmi12/Ex-1-NN/assets/138849182/99078f5a-a974-4892-aa8e-60122a1e7993)






## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


