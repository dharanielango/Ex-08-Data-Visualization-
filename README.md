# Ex-07-Data-Visualization-

## AIM
To Perform Data Visualization on a complex dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
```
import pandas as pd
import numpy as np
df=open('Superstore.csv', encoding='windows-1252')
df = pd.read_csv("Superstore.csv",encoding='windows-1254')
df.head()
```
# DATA VISTUALISATION USING SEABORN:
```
import seaborn as sns
from matplotlib import pyplot as plt
plt.figure(figsize=(8,5))
sns.lineplot(x="Segment",y="Region",data=df,marker='o')
plt.xticks(rotation = 90)
sns.lineplot(x='Ship Mode',y='Category', hue ="Segment",data=df)
sns.lineplot(x="Category",y="Sales",data=df,marker='o')
sns.scatterplot(x='Category',y='Sub-Category',data=df)
sns.scatterplot(x='Category', y='Sub-Category', hue ="Segment",data=df)
plt.figure(figsize=(10,7))
sns.scatterplot(x="Region",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.boxplot(x="Sub-Category",y="Discount",data=df)
sns.boxplot( x="Profit", y="Category",data=df)
sns.violinplot(x="Profit",data=df)
sns.barplot(x="Sub-Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.barplot(x="Category",y="Sales",data=df)
plt.xticks(rotation = 90)
sns.pointplot(x=df["Quantity"],y=df["Discount"])
sns.countplot(x="Category",data=df)
sns.countplot(x="Sub-Category",data=df)
sns.histplot(data=df,x ='Ship Mode',hue='Sub-Category')
sns.kdeplot(x="Profit", data = df,hue='Categor
```
# Data Visualization Using MatPlotlib
```
plt.plot(df['Category'], df['Sales'])
plt.show()
df.corr()
plt.subplots(figsize=(12,7))
sns.heatmap(df.corr(),annot=True)
df1=df.groupby(by=["Ship Mode"]).sum()
labels=[]
for i in df1.index:
    labels.append(i)
colors=sns.color_palette("bright")
plt.pie(df1["Sales"],labels=labels,autopct="%0.0f%%")
plt.show()
df3=df.groupby(by=["Category"]).sum()
labels=[]
for i in df3.index:
    labels.append(i) 
plt.figure(figsize=(8,8))
colors = sns.color_palette('pastel')
plt.pie(df3["Profit"],colors = colors,labels=labels, autopct = '%0.0f%%')
plt.show()
plt.hist(df["Sub-Category"],facecolor="peru",edgecolor="blue",bins=10)
plt.show()
plt.bar(df.index,df['Category'])
plt.show()
plt.scatter(df["Region"],df["Profit"], c ="blue")
plt.show() 
plt.boxplot(x="Sales",data=df)
plt.show()
```
# OUTPUT
## DATA VISTUALISATION USING SEABORN:
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/41.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/42.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/44.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/45.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/46.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/47.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/48.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/49.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/50.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/51.png)
## Data Visualization Using MatPlotlib
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/52.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/53.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/54.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/55.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/56.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/57.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/58.png)
![o](https://github.com/dharanielango/Ex-08-Data-Visualization-/blob/main/59.png)
# RESULT:
Hence,Data Visualization is applied on the complex dataset using libraries like Seaborn and Matplotlib successfully and the data is saved to file.
