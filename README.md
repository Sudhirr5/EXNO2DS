# EXNO2DS
# AIM:
     To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
NAME : SUDHIR KUAMR.R
REG NO : 212223230221
```
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
![Alt text](<Screenshot 2024-03-15 160957.png>)
```
df.info
```
![Alt text](<Screenshot 2024-03-15 161206.png>)
```
df.shape
```

![Alt text](<Screenshot 2024-03-15 161514.png>)
```
df.set_index("PassengerId,inplace=True)
df.head()
```
![Alt text](310891238-5561c748-5488-4344-bee1-3d485472ae20.png)
```
df.nunique()
```
![Alt text](310891430-6c8a9705-dec2-4c79-b679-7e7106aec017.png)

```
df["Survied"].value_counts()
```
![Alt text](310891448-a5b6b489-e8e2-4c0e-8d92-6e80c53ba2a8.png)

```
per=(df["Surived].value_counts()/df.shape[0]*100).round(3)
```
![Alt text](310891462-2ed9e63c-3393-434a-8c25-1bd372291679.png)
```
sna.countplot(data=df,x="Survived")
```
![Alt text](310893294-e7a6e7f2-69dd-4d8b-9c0f-5c5b77660059.png)
```
df
```
![Alt text](310893361-c9e68755-744f-46c4-b20c-4a9154e7f05e.png)
```
df.Pclass.nunique()
```
![Alt text](310893394-ac820af9-3415-493a-8168-171f1e99db37.png)

```
df.rename(columns={'Sex':'Gender'},inplace=True)
```
![Alt text](310893420-3654bd55-5377-43dd-9a5a-ed68954c0852.png)

```
sns.catplot(x='Gender',col='Survied',kind='count',data=df,height=5,aspect=.7)
```
![Alt text](310894057-2bb3728a-7b12-41ac-9181-b7dbc1550c2a.png)

```
sns.catplot(x='Surived',kind='count',hue='Gender',data=df)
```
![Alt text](310894126-d87f1acf-0fe1-4675-ab8e-903d5a1d8302.png)

```
df.boxplot(column='Age',by='Survived')
```
![Alt text](310894282-9c3b5bb5-f589-4ae4-a22d-8cdf16b4e700.png)

```
df.boxplot(column='Age',by='Survived')

```
![Alt text](<310894282-9c3b5bb5-f589-4ae4-a22d-8cdf16b4e700 (1).png>)

```
sns.scatterplot(x=df['Age'],y=df['Fare'])
```
![Alt text](310894362-0feda8e0-6bd6-4a55-a66f-62ca6a3b1acc.png)
```
sns.jointplot(x='Age',y='Fare',data=df)
```
![Alt text](310894435-eaf510e8-01f1-4f68-a306-c2d9be01956c.png)

![Alt text](310894556-610f0cc6-a567-4892-80c1-a20938fbc3b0.png)

```
sns.catplot(data=df,x='Gender',col='Survived',hue='Pclass',kind='count')
```
![Alt text](310894964-906ca836-c95a-4883-aa88-25e627549a23.png)

```
corr=dt.corr()
sns.heatmap(corr,annot=True)
```


![Alt text](310895047-32ca400f-a337-4319-9ec1-7774383f3f55.png)


```
sns.pairplot(df)
fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age,hue='gender',data=df)
```

![Alt text](310895144-08d7611c-6d6a-406f-98ca-30d3b0ca9266.png)       

# RESULT:
Thus the Exploratory Data Analysis process is performed successfully on the given data using python code.
