## Libraries used : Pandas, Numpy, Sci-learn kit, MatplotLib, Seaborn
## Data - 5 features with 3150 records
## Features 
* Rating - Ratings are between 1 - 5
* Data - Date when feedback was given
* Variation - Categorical column for appearance 
* Verified Reviews - Comments of the Customers
* Feedback - Categorical Column : Two categories - Positive(1) or Negative(0)

## Let's Explore the Dataset 
* Nulls - We don't have any nulls
* Basic Visulaization to understand the distribution of feedback column and rating column

  <img width="576" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/275472d2-ab01-4d10-9a4b-e56dfa377e18">

## Let's Visualize the length of the comments 

<img width="296" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/69dc57e4-642f-41d2-88ee-4fe1dde6b966">
* The longest message is of 2851 words and the shortest is of 1 word
* Average words in comments are 132 words

## Dividing data into 2 parts - Positive and Negative comments 
* Positive - 2893 records , Negative - 257 records
* Building a Word Cloud to understand the most frequent word used in comments
   
### Positive Word Cloud  

![image](https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/0c48566b-133d-417a-aeff-7d909ed65797)

## Negative WOrd Cloud 

![image](https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/cb9a9562-1173-4943-980e-14b7f2c864bd)

## Data Cleaning 
* Dropping 'Date', 'Rating', 'Length' columns
* We have 3 columns 'Variation', 'Verified_Reviews', Feedback

### Converting 'Variation' column into numbers 
* Applying Dummies

<img width="533" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/4e7b9cc7-d15b-4038-adcd-4dc49998fed4">

* Dropping variation column and concatenating dummy variables

## Cleaning Text of 'Verified_Reviews' column
### Created a new function for removing punctuations and stopwords 

<img width="788" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/475bced8-ae02-4401-a0b9-4ef67fb3f66a">

### Tokeinzing using Count Vectorizer

<img width="480" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/1abc54f2-38f9-46f3-95c9-c4d279ec9460">

* Combining all the X-variables
* Y - Variable is 'Feedback' column

## TRAINING A NAIVE BAYES CLASSIFIER MODEL

<img width="427" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/dfeb210c-8ef5-4537-bb64-707d85fab766">

### Confusion Matrix on train data

<img width="268" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/5a279042-0602-4af1-98cc-ade272501446">

### Confusion Matrix on test data

<img width="263" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/a12d666e-2ed2-4f4e-9c88-8feb21ba4864">

#### Classification Report 

<img width="325" alt="image" src="https://github.com/Aniket2k15/Customer-Reviews/assets/138878014/1a4c51b0-72f3-4276-8c47-14704559659b">

















  
