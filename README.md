# Debuggers
Bancolombia Dataton Code from the [Kaggle Competition](https://www.kaggle.com/c/datatonbc-2020), where you can see the rules and download the data that was given to solve the problem

# How much is the family monthly expense of each Bancolombia customers? 

To face this problem we explore three ways to master the data and make the final dataset to training the models

## Data Engineering

  We fist have to fix the [numerical](https://github.com/DLesmes/Debuggers/blob/main/80%25/Numerical_Data_Engineering.ipynb) and the [categorical](https://github.com/DLesmes/Debuggers/blob/main/80%25/Categorical_Data_Engineering.ipynb) data, and make some categorical ranks to [label](https://github.com/DLesmes/Debuggers/blob/main/80%25/Labeled%26Dummies_Variables.ipynb) the data focused on the objective variable, but [here](https://github.com/DLesmes/Debuggers/blob/main/80%25/Alomarrano_processing/Data_Engineering.ipynb) you can see a kind of EDA

1. Aggregate all data per user id

  [Here](https://github.com/DLesmes/Debuggers/blob/main/80%25/Calculo%20por%20mes.ipynb) is the code used to reach this objective. At the very beggining of this process the idea was to set the money variables in dic-20 value [here](https://github.com/DLesmes/Debuggers/blob/main/80%25/Indexing_Input_Pesos_Dic_20.ipynb) based on the [IPC](https://totoro.banrep.gov.co/analytics/saw.dll?Download&Format=excel2007&Extension=.xls&BypassCache=true&lang=es&NQUser=publico&NQPassword=publico123&path=%2Fshared%2FSeries%20Estad%C3%ADsticas_T%2F1.%20IPC%20base%202018%2F1.2.%20Por%20a%C3%B1o%2F1.2.5.IPC_Serie_variaciones)

2. Aggregate all data per month

  [Here](https://github.com/DLesmes/Debuggers/blob/main/80%25/Aggregate_all_dataXid.ipynb) is the code used to reach this objective

3. Take historical data along the timeline

  [Here](https://github.com/DLesmes/Debuggers/blob/main/80%25/Alomarrano_processing/Categorical_Data_Engineering-Copy1.ipynb) is the code to reach this objective

In each case we have to impute all the missing values with the [PPCA](https://www.rdocumentation.org/packages/pcaMethods/versions/1.64.0/topics/ppca) R method [here](https://github.com/DLesmes/Debuggers/blob/main/PPCA4missing_values.R) and verificate the results here

* Per [user Id](https://github.com/DLesmes/Debuggers/tree/main/80%25) 
* Per [month](https://github.com/DLesmes/Debuggers/blob/main/80%25/Xmes_MissingValuesAnalysis.ipynb)
* Per [all timeline](https://github.com/DLesmes/Debuggers/blob/main/80%25/Alomarrano_processing/Xmes_MissingValuesAnalysis-Copy1.ipynb)

## Data Science

To modeling the problem we follow this steps

1. Correlations analysis, [this](https://github.com/DLesmes/Debuggers/blob/main/20%25/LinearRegresion.ipynb) was the one done in the data per id

2. Linear regression

* Per [user Id](https://github.com/DLesmes/Debuggers/blob/main/20%25/Xid_LinearRegresion.ipynb)
* per [month](https://github.com/DLesmes/Debuggers/blob/main/20%25/Xmes_LinearRegresion.ipynb)
* Per [all timeline](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/Xid_LinearRegresion-Copy1.ipynb)

3. PCA

* Per [user Id](https://github.com/DLesmes/Debuggers/blob/main/20%25/Xid_PCA.ipynb)
* per [month](https://github.com/DLesmes/Debuggers/blob/main/20%25/Xmes_PCA.ipynb)
* Per [all timeline](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/Xid_PCA-Copy2.ipynb)

4. [Tree algorithms](https://github.com/DLesmes/Debuggers/blob/main/20%25/Modeling_GridSearchRandomForest.ipynb)

5. Neuronal Networs ([1st](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/NN_littlePig.ipynb), [2nd](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/NN_littlePig_Arqui_2.ipynb), [3rd](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/NN_littlePig_Arqui_3.ipynb), [4th](https://github.com/DLesmes/Debuggers/blob/main/20%25/Alomarrano/NN_littlePig_Arqui_3_Znorm.ipynb))

We did't win but we learn too much! 

# Variables 

![](https://lh3.googleusercontent.com/-VUl5Px1FM44/YAHrCk-mxEI/AAAAAAAA7K0/ol5P4_yDVa8TO0xW4FFnLINyMWkl5YF5gCK8BGAsYHg/s0/2021-01-15.png)
![](https://lh3.googleusercontent.com/-12r2ykYakkU/YAHrRl3kwyI/AAAAAAAA7K4/QnUGZ7-9-_0nq-b7HHNYTQwQF3mdD1rfwCK8BGAsYHg/s0/2021-01-15.png)
![](https://lh3.googleusercontent.com/-MKVLaMtWpuI/YAHrdbrnlsI/AAAAAAAA7LA/3xljQ_CBm1oCOMTDruuKMIdbvawZ5_VngCK8BGAsYHg/s0/2021-01-15.png)
![](https://lh3.googleusercontent.com/-gEf2taTwiok/YAHrrG7oAeI/AAAAAAAA7LE/vGvhfli0-2An715-4vw3F79glbb5uTrPwCK8BGAsYHg/s0/2021-01-15.png)
