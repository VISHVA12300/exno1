# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv('/content/SAMPLEIDS.csv')
df
df.head()
df.tail()
```
![IMG-20240223-WA0002](https://github.com/VISHVA12300/exno1/assets/119404426/d79094e9-01f3-4e0a-a900-b9681cb77801)

```
df.info()
```
![WhatsApp Image 2024-02-23 at 15 59 34_38cecad5](https://github.com/VISHVA12300/exno1/assets/119404426/94e37c95-f449-42a3-9b08-65d6c5661679)

```
df.describe()

```
![IMG-20240223-WA00042](https://github.com/VISHVA12300/exno1/assets/119404426/bc21af52-598d-4fa6-9606-6749226f6054)

```
df.shape()

```
![IMG-20240223-WA00043](https://github.com/VISHVA12300/exno1/assets/119404426/73695c08-1f26-4d60-8229-38fd0f56f099)

```
df.isnull.sum()

```
![IMG-20240223-WA00044](https://github.com/VISHVA12300/exno1/assets/119404426/7c42ad66-1133-416f-a590-a2a7acd33709)

```
x=df.dropna(how='any')

```
![IMG-20240223-WA00031](https://github.com/VISHVA12300/exno1/assets/119404426/3b9b6d31-f38d-4ba7-aa7c-f2ed1557614f)

```
df.fillna(0)

```
![IMG-20240223-WA0005](https://github.com/VISHVA12300/exno1/assets/119404426/59ab1cf9-4dab-4e3a-981d-a5784ccd709b)

```
mn=df.TOTAL.mean()
mn
```
![WhatsApp Image 2024-02-23 at 15 59 35_679250fc](https://github.com/VISHVA12300/exno1/assets/119404426/2002abe5-3ee6-4d1f-a0bd-4445c52f12b8)

```
df.TOTAL.fillna(mn,inplace=True)
for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df
```
![IMG-20240223-WA00082](https://github.com/VISHVA12300/exno1/assets/119404426/44167011-f625-456c-b025-ca1440ef844f)








            
# Result
The dta clearning has been done successfully.
          <<include your Result here>>
