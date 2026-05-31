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
```py
import pandas as pd 
import seaborn as sns 
import matplotlib.pyplot as plt 
df=pd.read_csv("titanic_dataset.csv") 
df.head()
```
<img width="949" height="162" alt="image" src="https://github.com/user-attachments/assets/0973f5d4-cae9-4972-9301-62aeabc6f4db" />

```py
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="821" height="655" alt="image" src="https://github.com/user-attachments/assets/43ebaafc-14bf-4766-b854-ad734b50c2e4" />

```py
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="833" height="654" alt="image" src="https://github.com/user-attachments/assets/44fe9fbd-3e86-43ff-8021-b8bdc1dc313c" />

```py
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```

<img width="954" height="653" alt="image" src="https://github.com/user-attachments/assets/0e000179-a29e-4288-acf2-e87f41b4ae3d" />

```py
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare') plt.show()
```
<img width="804" height="631" alt="image" src="https://github.com/user-attachments/assets/0a3122a7-4afd-4f50-9879-b13681766d4f" />

```py
sns.kdeplot(data=df['Age'], shade=True)
 plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="900" height="688" alt="image" src="https://github.com/user-attachments/assets/b98c3f04-2ce9-45d1-a747-b636ed927679" />

```py
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="842" height="687" alt="image" src="https://github.com/user-attachments/assets/1476e0c5-5fa0-49fc-92bc-8e8637482b30" />

# Result:

Thus the given experiment verified succesfully using jupyter note book
