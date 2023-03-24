# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# EXPLANATION
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data.csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```

# OUTPUT

## DATA

![s1](https://user-images.githubusercontent.com/128135934/227517269-7dc23806-cd13-4b55-88a0-d79fa6f165de.png)
![s2](https://user-images.githubusercontent.com/128135934/227517350-101f12cd-b278-4f67-bab2-c939d321c345.png)

## NON NULL BEFORE

![s3](https://user-images.githubusercontent.com/128135934/227517421-fc6781b0-3430-451f-b161-87d27665f6d4.png)
![s4](https://user-images.githubusercontent.com/128135934/227517473-1253759e-6e3a-47df-bd9b-8ed99fb04d7c.png)
![s5](https://user-images.githubusercontent.com/128135934/227517506-f7de5874-d18e-40f7-b984-398227b52449.png)

## MODE

![s6](https://user-images.githubusercontent.com/128135934/227517638-9241c19d-d900-403b-81c2-733827b7d3fd.png)

## MEAN

![s7](https://user-images.githubusercontent.com/128135934/227517701-64675474-98ce-4f5d-b36a-3bb8eab288ff.png)

## MEDIAN

![s8](https://user-images.githubusercontent.com/128135934/227517756-c027e2d9-a8f2-4d4b-845e-4715388eddac.png)

## NON NULL AFTER

![s9](https://user-images.githubusercontent.com/128135934/227517837-f8c13125-0f85-4fdf-92bc-4375ed8876ab.png)
![s10](https://user-images.githubusercontent.com/128135934/227517856-226d6649-21a5-4c29-9786-55e55dc2533e.png)

# RESULT
Thus,the given data is read,clensed and the cleansed data is saved into the file.
