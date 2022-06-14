# Salary Prediction Portfolio

## Define the Problem

### Project Goal: 
The goal of this project is to predict the salary based on various factors like jobtype, degree, subject major in terms of education, type of industry, years of experience and miles from metropolis.

### Practical use: 
This model can help job searchers determine whether a job listing offers a reasonable salary based on the requirements and distinct characteristics compared to other jobs with similar requirements and characteristics. Additionaly, this model Can be used by the government to analyse the trends in job market/economy growth and salary range to the corresponding related jobs.

### Tool: 
Python 3 (Jupyter Notebook) with a wide range of libraries/packages available for data manipulation and predictive modeling algorithms.


## Datasets:

train_features.csv: Each row represents an observation for each individual job posting. The "jobId" column is unique to each job posting and the other columns are the different features of the job postings. The file has eight(8) columns.

train-salaries.csv: Each row is a unique job posting with its corresponding salary. The file contains two (2) columns. The file is combined with train_features.csv to train the machine learning models.

test_features.csv: Similar to train_features.csv, each row in this file is metadata for each individual job posting. The file has eight (8) columns and is used to predict the new salaries.


## Feature structure

jobId: Distinct key that identifies each job listing

companyId: Distinct key that identifies each company

jobType: Defines the level of the position

degree: Represents the education level requirement

major: Identifies the desired major for the job listing

industry: Characterizes the specific industry of the job listing

yearsExperience: Designates the required years of experience for the job listing

milesFromMetropolis: Specifies the distance the job listing is from the center of the metropolis


## Exploratory Data Analysis

1- Import Libraries 

2- Load Data

3- Examine and Get Insights on Data

4- The 3 input files each have 1 million rows.
      
      Merged train data (train_features + train_target) which has 1 million rows and 9 columns
      
      Test Feature data has 1 million rows and 8 columns
      
      Datasets have mixed data types (categorical and numerical)

5- Clean data
     - No duplicates in data
     
     - Datasets do not have null values
     
     - Check for invalid data - Dropped 5 rows of data with invalid Salary (salary less than or equal to 0)

6- Explore data

7- Summarize Numerical and Categorical variables 

8- Visualize the target variable using plots 

9- Check for outliers

10- Review Correlation between each feature and the target variable using plots and feature counts as required

11- Identify correlation between all features respectively by using label encoding categorical features with the mean salary

12- Set baseline model
   
   Using the correlation martix, identified the highest correlated feature and use this to build a simple linear regression model to predict the salary,      using mean squared error as the quality of an estimator. The  MSE is 963.9252996562975

13- Model development
    
    - Linear Regression
    - Random Forest Regressor
    - Gradient Boosting Regressor
    
    
## Feature Summary

### Salary vs jobType
<img width="925" alt="Screen Shot 2022-06-13 at 11 17 39 PM" src="https://user-images.githubusercontent.com/104243935/173486202-8a645201-9484-459a-8d16-a1a69437e817.png">

There is a relationship between salaries and job types as CEO,CFO,CTO have higher salaries compared to other job types

### Salary vs degree
<img width="902" alt="Screen Shot 2022-06-13 at 11 19 49 PM" src="https://user-images.githubusercontent.com/104243935/173486470-3fbd64ea-6d57-48a8-99d4-5f24b72d2b2f.png">

There is a relationship between salaries and degree types as people with More advanced degrees have higher salaries

### Salary vs major
<img width="948" alt="Screen Shot 2022-06-13 at 11 21 46 PM" src="https://user-images.githubusercontent.com/104243935/173486637-f62491ce-3eab-44c9-8982-f8076914ca1a.png">

People with majors of engineering, business and math have higher salaries

### Salary vs industry
<img width="932" alt="Screen Shot 2022-06-13 at 11 24 54 PM" src="https://user-images.githubusercontent.com/104243935/173486982-e26752d4-ed19-4355-9242-955a6b059011.png">

people who work in the finance and oil industries have higher salaries

### Years of Experience Feature
<img width="924" alt="Screen Shot 2022-06-13 at 11 26 45 PM" src="https://user-images.githubusercontent.com/104243935/173487166-5d0b9c96-8a68-4bf5-a24c-01f2ea2c4169.png">

There is a positve relationship between salaries and number of years experience. The more experience you have, the higher the salary

### Miles From Metropolis Feature
<img width="918" alt="Screen Shot 2022-06-13 at 11 28 14 PM" src="https://user-images.githubusercontent.com/104243935/173487399-14668d47-5c12-44d3-bb90-849a19349ee1.png">

There is a negative relationship between salaries and number of miles from Metropolis. the further you live from Metropolis, the lower the salary you would receive


## Correlation Matrix

<img width="776" alt="Screen Shot 2022-06-13 at 11 30 41 PM" src="https://user-images.githubusercontent.com/104243935/173487618-0c2fab2f-b527-43a7-b2a4-65793e645f9b.png">

Job type has the strongest correlation with salary
Major and degree are the most correlated. They have a positive correlation


## Models

<img width="494" alt="Screen Shot 2022-06-13 at 11 33 33 PM" src="https://user-images.githubusercontent.com/104243935/173487912-9ef5151d-c5c2-40a6-844d-40930c61aa3a.png">

The best model is Random Forest because it has the low mean squared error compared to the other models

## Predictions

<img width="273" alt="Screen Shot 2022-06-13 at 11 35 44 PM" src="https://user-images.githubusercontent.com/104243935/173488128-55ee6a62-554c-4d21-80fd-c2754d025300.png">

## Feature Importance

<img width="1002" alt="Screen Shot 2022-06-13 at 11 36 42 PM" src="https://user-images.githubusercontent.com/104243935/173488209-f3d1e387-702c-4c08-a2ea-c3ad3052ac1d.png">

 The most important features are years of experience and miles from metropolis.  
    


