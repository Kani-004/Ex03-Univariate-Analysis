Ex03-Univariate-Analysis

Aim:

To perform Univariate EDA on the given data set

Explanation:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis

Algorithm

STEP 1

Import the built libraries required to perform EDA and outlier removal.

STEP 2

Read the given csv file

STEP 3

Convert the file into a dataframe and get information of the data.

STEP 4

Return the objects containing counts of unique values using (value_counts()).

STEP 5

Plot the counts in the form of Histogram or Bar Graph.

STEP 6

Use seaborn the bar graph comparison of data can be viewed.

STEP 7

Save the final data set into the file

Program

Name:kanimozhi
Reg no:212221220024

import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)
*/


Output:

Dataset:

![image](https://user-images.githubusercontent.com/129577149/229985666-53d389bd-4cd4-44ae-a194-1e10a6488a9c.png)


Head:

![image](https://user-images.githubusercontent.com/129577149/229986002-fc65b1ab-9117-441e-abca-ed2eb69ce808.png)

Info:

![image](https://user-images.githubusercontent.com/129577149/229986060-4badcca2-98ce-4275-ae4d-54eb402f9242.png)

Describe:

![image](https://user-images.githubusercontent.com/129577149/229986234-42b9d552-d83b-44ff-ab7a-a0a7a8951ecc.png)


Isnull:

![image](https://user-images.githubusercontent.com/129577149/229986296-4d0bf5de-c0c7-425e-bf0e-060c18593777.png)

dtypes:

![image](https://user-images.githubusercontent.com/129577149/229986366-2d11e52f-8fda-4db8-9e13-b70745480654.png)


Value count:

![image](https://user-images.githubusercontent.com/129577149/229986414-5b07d8af-8794-4802-a51b-5cd03d121aa2.png)

Boxplot:

![image](https://user-images.githubusercontent.com/129577149/229986479-aa9a4bf9-73cb-4a32-9ea2-58799660f5e3.png)

Countplot:

![image](https://user-images.githubusercontent.com/129577149/229986542-517e3b45-08a5-4861-8b89-f05d0df10ccc.png)

Distribution plot:

![image](https://user-images.githubusercontent.com/129577149/229986625-2693ede2-b267-43b5-a02a-78c562fe8584.png)


Histogram plot:

![image](https://user-images.githubusercontent.com/129577149/229986676-f9460fa8-134b-477e-98be-064c67aca36d.png)

Result:

Thus we have read the given data and performed the univariate analysis with different types of plots.








