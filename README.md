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
      import pandas as pd 
      import numpy as np
      import seaborn as sns
      df = pd.read_csv("/content/titanic_dataset.csv")
      df     
<img width="1314" height="614" alt="image" src="https://github.com/user-attachments/assets/dd4b39c0-8675-441d-b96f-ecedae1cbe3f" /> 

      df.info()        
<img width="529" height="428" alt="image" src="https://github.com/user-attachments/assets/54985929-457d-4997-a87a-d6b6dcc69e18" />  

      df.describe()  
<img width="873" height="363" alt="image" src="https://github.com/user-attachments/assets/81a8c6f5-dcd7-4d87-82b2-fd4ee6a0199d" />   

      df.dtypes
<img width="213" height="555" alt="image" src="https://github.com/user-attachments/assets/d1c1067d-66af-4283-9d41-c472317f1dae" />   

      df.shape    
<img width="158" height="46" alt="image" src="https://github.com/user-attachments/assets/23575dd1-7e1d-4951-b0f4-fc2363a4f184" />     

      df.value_counts()    
<img width="1593" height="522" alt="image" src="https://github.com/user-attachments/assets/2a28dcfa-bab4-412b-8430-d78da38d671a" />     

      df['Age'].value_counts()   
<img width="193" height="544" alt="image" src="https://github.com/user-attachments/assets/c813fc54-8f8f-4b26-b20e-387d56dc26b0" />    

      df.set_index("PassengerId", inplace=True)     
      df   
<img width="1444" height="533" alt="image" src="https://github.com/user-attachments/assets/b9e775a3-2ea8-4037-be48-96b3fbfda8d7" />     

      df.nunique()
<img width="185" height="531" alt="image" src="https://github.com/user-attachments/assets/e848ad6e-f01a-4977-a5f0-b3921aa23844" />   

      sns.countplot(data=df, x="Age")
<img width="818" height="574" alt="image" src="https://github.com/user-attachments/assets/4d3b5f7c-5636-4aa0-b159-703089da8802" />    

      sns.countplot(data=df, x="Survived")
<img width="798" height="563" alt="image" src="https://github.com/user-attachments/assets/08b3ed88-e926-4366-9718-8936719a0218" />    

      df.rename(columns={'Sex':'Gender'},inplace=True)
      df
<img width="1584" height="555" alt="image" src="https://github.com/user-attachments/assets/c4464d59-dd45-4985-a46a-38dab4176e2b" />    

      sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
<img width="973" height="633" alt="image" src="https://github.com/user-attachments/assets/cecb6cb3-6b06-4af2-835b-0cd698b31124" />    

      df.boxplot(column="Age", by="Survived")
<img width="897" height="614" alt="image" src="https://github.com/user-attachments/assets/c30faaca-6d77-4df2-a92a-70cb59d5ea4b" />    

      sns.scatterplot(x=df["Age"], y=df["Fare"])
<img width="833" height="558" alt="image" src="https://github.com/user-attachments/assets/11d1a7c8-bbdd-4c4b-998e-b5c0b2f92461" />    

      plt = sns.boxplot(x='Pclass', y='Age', hue='Gender', data=df)
<img width="727" height="543" alt="image" src="https://github.com/user-attachments/assets/03c3639d-33a1-4ee2-9665-9e5a88529c15" />    

      import seaborn as sns
      sns.catplot(x='Pclass', y="Age", hue="Gender", col="Survived", kind="box", data=df)
<img width="1580" height="653" alt="image" src="https://github.com/user-attachments/assets/6d8bf6f9-f52d-4bee-bf74-ee10797246cf" />    

      corr = df.corr(numeric_only=True)
      sns.heatmap(corr, annot=True)
<img width="693" height="547" alt="image" src="https://github.com/user-attachments/assets/4d3d06f2-f5ff-4f6f-a73e-317eabd821ce" />


# RESULT
        <<INCLUDE YOUR RESULT HERE>>
