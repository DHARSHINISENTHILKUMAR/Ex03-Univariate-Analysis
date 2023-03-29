# Ex03-Univariate-Analysis
# Aim:
## To perform Univariate EDA on the given data set
# Explanation:
## Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis
# Algorithm
# STEP 1 
## Import the built libraries required to perform EDA and outlier removal.

# STEP 2 
## Read the given csv file

# STEP 3 
## Convert the file into a dataframe and get information of the data.

# STEP 4 
## Return the objects containing counts of unique values using (value_counts()).

# STEP 5 
## Plot the counts in the form of Histogram or Bar Graph.

# STEP 6 
## Use seaborn the bar graph comparison of data can be viewed.

# STEP 7
## Save the final data set into the file
# Program
~~~
Name:Dharshini S
Reg no:212221220009
~~~
~~~
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
~~~
# Output:
# Dataset:
![image](https://user-images.githubusercontent.com/113699377/228594132-e71945f2-f085-4bed-90e1-54717a7ce619.png)
# Head:
![image](https://user-images.githubusercontent.com/113699377/228594278-f8335696-4461-4680-b018-4ee9c479ab12.png)
# Info:
![image](https://user-images.githubusercontent.com/113699377/228594366-831712b2-0f54-4360-a5fa-82904e8d93a7.png)
# Describe:
![image](https://user-images.githubusercontent.com/113699377/228594471-c89da132-0d38-4fa0-a336-28d874f4d449.png)
# Isnull:
![image](https://user-images.githubusercontent.com/113699377/228594621-679835cb-0b4f-4ca8-a521-855a0559ccf0.png)
# dtypes:
![image](https://user-images.githubusercontent.com/113699377/228594702-71f04476-7a35-4cb4-913f-85964f1ef166.png)
# Value count:
![image](https://user-images.githubusercontent.com/113699377/228594792-f3329d3c-2421-4895-ae14-d1db6a2b149b.png)
# Boxplot:
![image](https://user-images.githubusercontent.com/113699377/228594852-90b71897-d9ea-40c9-8f06-2e73d21653a5.png)
# Countplot:
![image](https://user-images.githubusercontent.com/113699377/228594946-3b1aeb21-5a0b-4eb5-b744-47f7076a326b.png)
# Distribution plot:
![image](https://user-images.githubusercontent.com/113699377/228595076-7a1c39c7-40a0-42a1-bfa9-50d17b7cd7c8.png)
# Histogram plot:
![image](https://user-images.githubusercontent.com/113699377/228595163-eb8d4aa5-8541-4685-8d71-a0ab94bf95a7.png)
# Result:
### Thus we have read the given data and performed the univariate analysis with different types of plots.

