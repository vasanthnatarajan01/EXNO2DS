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

## CODING AND OUTPUT:
```import pandas as pd 
import numpy as np
import seaborn as sns
df = pd.read_csv("/content/titanic_dataset.csv")
df````
<img width="1314" height="614" alt="image" src="https://github.com/user-attachments/assets/dd4b39c0-8675-441d-b96f-ecedae1cbe3f" />
```df.info()```
<img width="529" height="428" alt="image" src="https://github.com/user-attachments/assets/54985929-457d-4997-a87a-d6b6dcc69e18" />
```df.describe()```
<img width="873" height="363" alt="image" src="https://github.com/user-attachments/assets/81a8c6f5-dcd7-4d87-82b2-fd4ee6a0199d" />
```df.dtypes```
<img width="213" height="555" alt="image" src="https://github.com/user-attachments/assets/d1c1067d-66af-4283-9d41-c472317f1dae" />
```df.shape```
<img width="158" height="46" alt="image" src="https://github.com/user-attachments/assets/23575dd1-7e1d-4951-b0f4-fc2363a4f184" />
```df.value_counts()```
<img width="1593" height="522" alt="image" src="https://github.com/user-attachments/assets/2a28dcfa-bab4-412b-8430-d78da38d671a" />
```df['Age'].value_counts()```
<img width="193" height="544" alt="image" src="https://github.com/user-attachments/assets/c813fc54-8f8f-4b26-b20e-387d56dc26b0" />
```df.set_index("PassengerId", inplace=True)
df```
<img width="1444" height="533" alt="image" src="https://github.com/user-attachments/assets/b9e775a3-2ea8-4037-be48-96b3fbfda8d7" />
```df.nunique()```

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
