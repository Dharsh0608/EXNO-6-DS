# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

```
 import pandas as pd
 import seaborn as sns
 import matplotlib.pyplot as plt
 df=pd.read_csv("titanic_dataset.csv")
 df.head()
```
<img width="825" height="194" alt="image" src="https://github.com/user-attachments/assets/741b7873-a091-449b-a002-253356e5e76d" />

# Line plot:
```
 x=[1,2,3,4,5]
 y=[3,6,2,7,1]
 sns.lineplot(x=x,y=y)
 plt.title('Line Plot')
```
<img width="433" height="352" alt="image" src="https://github.com/user-attachments/assets/4b6345b4-702a-49d5-b5dd-2933cb0ea8bc" />


# Multi Line Plot:
```
 x=[1,2,3,4,5]
 y1=[3,5,2,6,1]
 y2=[1,6,4,3,8]
 y3=[5,2,7,1,4]
 sns.lineplot(x=x,y=y1)
 sns.lineplot(x=x,y=y2)
 sns.lineplot(x=x,y=y3)
 plt.title('Multi Line Plot')
```
<img width="442" height="352" alt="image" src="https://github.com/user-attachments/assets/1a93cbff-2918-412f-a51a-b1e9f4196eeb" />


#TO VISUALIZE RELATIONSHIPS
# Bar Chart:
```
 plt.figure(figsize=(8,5))
 sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
 plt.title("Fare Of Passenger By Embarked Town")
```
<img width="574" height="397" alt="image" src="https://github.com/user-attachments/assets/9ef6fc59-cd08-4708-8257-b3078848529f" />


# Scatter Plot:
```
 sns.scatterplot(x="Age", y="Fare", data=df)
 plt.title('Scatterplot of Age vs Fare')
 plt.show()
```
<img width="516" height="354" alt="image" src="https://github.com/user-attachments/assets/902011a9-be05-4196-88d1-6470000550ab" />


# Bubble Chart:
```
 sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
 plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
 plt.show()
```
<img width="523" height="355" alt="image" src="https://github.com/user-attachments/assets/e5e4ad2b-2682-42b2-8fa0-c6838a85b4c6" />


TO CAPTURE DISTRIBUTIONS

# Histogram:
```
 sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="505" height="347" alt="image" src="https://github.com/user-attachments/assets/1578a386-9a9c-47ca-8244-2be32aed2e13" />

# Box Plot:

```
 sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
 plt.title("Age By Passenger Class")
```
<img width="525" height="384" alt="image" src="https://github.com/user-attachments/assets/8687239e-79b3-4113-90c5-a5a37ada6b2d" />


# Violin Plot:
```
<img width="525" height="384" alt="image" src="https://github.com/user-attachments/assets/85ee8360-94ad-462f-83f7-3899dc293c4e" />

```
<img width="522" height="358" alt="image" src="https://github.com/user-attachments/assets/454eac81-aa3e-4d0f-a6e3-319f2b2e252e" />


# Density Plot:

```
 sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
 plt.show()
```
<img width="525" height="368" alt="image" src="https://github.com/user-attachments/assets/943e8029-b1b5-4625-a271-338ff1839f3b" />

# Heat Map:
```
 numeric_df = df.select_dtypes(include=['float64', 'int64'])
 corr_matrix = numeric_df.corr()
 sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
 plt.title('Heatmap of Titanic Dataset')
 plt.show()
```
<img width="515" height="390" alt="image" src="https://github.com/user-attachments/assets/1f8e8995-3e05-4e9d-93bd-2d493badc002" />

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
