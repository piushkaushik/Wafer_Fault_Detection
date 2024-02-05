# Wafer Fault Detection Project
![Silicon-Wafers](https://github.com/piushkaushik/Wafer_Fault_Detection/assets/95517586/fe84685b-8916-4876-a767-f81c0a32b0f6)

**I developed this project with the help of iNeuron.ai, showcasing my proficiency and practical application of skills in a professional setting.**
## Problem Statement:
The challenge at hand involves leveraging data collected from diverse sensors across multiple wafers used in electronic manufacturing. A wafer, essentially a thin semiconductor slice, serves as a crucial component in the production of integrated circuits. The objective is to construct a robust machine learning model capable of predicting the operational status of a given wafer, discerning whether replacement is necessary. The provided dataset comprises inputs from various sensors, and the binary classification task involves assigning one of two classes: +1, indicating that the wafer is in optimal working condition and does not require replacement; or -1, signifying a faulty wafer that necessitates replacement. The overarching goal is to develop a predictive model that enhances the efficiency of quality control in semiconductor manufacturing processes.

## Dataset:
For each wafer in consideration, data is sourced from an array of 500+ sensors. Subsequently, an evaluation is conducted to determine the operational status of the wafer, assigning it a classification of either +1 (indicating optimal functionality) or -1 (indicating a faulty condition). To access the dataset used in this analysis, kindly [Click Here to Access Data](https://drive.google.com/drive/folders/1BOnv-jyPS7vHz7vQv2otD0_GNZ0TL6yu?usp=drive_link).

## Architecture:
![Architecture](https://github.com/piushkaushik/Wafer_Fault_Detection/assets/95517586/94da8c90-5c7c-4b0e-8db3-75eb0782666b)

## Data Validation:
During this phase, a series of validation procedures are executed, encompassing checks for the validity of the filename, the presence of all required columns, the accurate nomenclature of each column, and the verification of the data type for each individual column. These meticulous steps ensure the integrity and accuracy of the dataset under consideration.

## Data Insertion in database:
During this stage, the following actions are undertaken:

- Database creation and establishment of a connection.
- Formulation of tables within the database.
- Systematic insertion of files into the designated tables.
This process ensures the structured and organized incorporation of data into the database, facilitating efficient data management and retrieval.

# Model Training:
## Data Extraction for Model Training:
The information residing within a stored database is extracted in the form of a CSV file, with the intention of utilizing it for the training of machine learning models. This systematic extraction process serves to prepare and format the data in a manner conducive to effective model training procedures.

## Data Preprocessing Procedures:
During this phase, a comprehensive assessment is conducted to identify and address null values within each column. In instances where null values are detected, the K-Nearest Neighbors (KNN) Imputer is employed to impute missing values, utilizing the mean of k neighbors for accurate replacement.
Additionally, a refinement process involves the removal of columns exhibiting a standard deviation of 0. This criterion indicates that all values within a particular column are identical, rendering the column devoid of meaningful variation for model training. Consequently, the elimination of such columns enhances the efficiency and relevance of the dataset for subsequent modeling endeavors.

## Cluster Analysis:
This step involves identifying similar entries in a dataset to form distinct clusters, enabling the training of separate models for each cluster. Utilizing K-Means on preprocessed data enhances accuracy by grouping similar data. The resulting models are saved for future use, optimizing overall efficiency and adaptability.

## Model Selection:
In this phase, post cluster creation, optimal models for each cluster are determined. Employing RandomForest and XGBoost algorithms, Grid Search CV is conducted to identify the best parameters for both models. Subsequently, model accuracies are compared, facilitating the selection of the superior-performing model...

## Model Prediction:

In the Model Prediction phase, encompassing Data Validation, Database Data Insertion, Data Preprocessing, and Clustering, models are selectively loaded based on cluster assignments. Subsequently, predictions are generated, completing the comprehensive workflow to predict outcomes tailored to the distinct characteristics of each data cluster.

