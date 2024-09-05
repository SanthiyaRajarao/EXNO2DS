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
REG NO : 212223230192
NAME : SANTHIYA R
```
```
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
![Screenshot 2024-09-05 213804](https://github.com/user-attachments/assets/9372ec79-bc1c-42b7-aee4-c4d02027761b)
```
df.isnull().sum()
```
![Screenshot 2024-09-05 213813](https://github.com/user-attachments/assets/b5cab503-32e4-49d6-b08f-6d9e6db76a84)
```
df.dropna(inplace=True)
df
```
![Screenshot 2024-09-05 213828](https://github.com/user-attachments/assets/1dcc51be-ad4d-4fe2-95bf-4f6ecd7b662b)
```
df.isnull().sum()
```
![Screenshot 2024-09-05 213837](https://github.com/user-attachments/assets/b07c8b2e-e016-4c23-8c4e-cf64362f1210)
```
df.info()
```
![Screenshot 2024-09-05 213856](https://github.com/user-attachments/assets/783c9a00-840a-4010-ba77-3938965a2f44)
```
df.shape
```
![Screenshot 2024-09-05 213904](https://github.com/user-attachments/assets/dada86d0-4bed-4f87-9927-9f53610b0511)
```
df.set_index("PassengerId",inplace=True)
df.describe()
```
![Screenshot 2024-09-05 213916](https://github.com/user-attachments/assets/2e492156-7da0-4392-8262-6c8505c70689)
```
df
```
![Screenshot 2024-09-05 213932](https://github.com/user-attachments/assets/7e6e4256-55ac-41f2-8713-d195c1fd5649)

```
df.nunique()
```
![Screenshot 2024-09-05 213942](https://github.com/user-attachments/assets/9ea80252-77bc-4264-8047-987364567163)
```
df["Survived"].value_counts()
```
![Screenshot 2024-09-05 213950](https://github.com/user-attachments/assets/64c12690-4c57-4c4f-bc9c-bbeb961687ec)
```
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```
![Screenshot 2024-09-05 213957](https://github.com/user-attachments/assets/9b8c55d1-ac66-4200-9dec-97c4c45ad522)
```
import matplotlib.pyplot as plt
import seaborn as sns
sns.countplot(data=df,x="Survived")
```
![Screenshot 2024-09-05 214008](https://github.com/user-attachments/assets/4fe81911-c5b1-4e45-9e74-07963769ab2e)
```
df.Pclass.unique()
```
![Screenshot 2024-09-05 214018](https://github.com/user-attachments/assets/c43d59e9-4606-4094-a8c3-8878200658b0)
```
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
![Screenshot 2024-09-05 214036](https://github.com/user-attachments/assets/a5ac9a9e-f12b-4c57-9dba-062ce6af975b)
```
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
```
![Screenshot 2024-09-05 214051](https://github.com/user-attachments/assets/9e66f2f1-4511-48d7-bbf8-b0ef59bb6caf)
```
sns.catplot(x="Survived",hue="Gender",data=df,kind="count")
```
![Screenshot 2024-09-05 214108](https://github.com/user-attachments/assets/37e76fc7-17fa-4ea9-abb3-078a63420a3a)
```
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![Screenshot 2024-09-05 214137](https://github.com/user-attachments/assets/d0397c0c-af90-4158-9ac5-4eb9b6eb10c1)

# RESULT
The Exploratory Data Analysis on the given data set has been performed.
