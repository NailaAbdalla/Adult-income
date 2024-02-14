# Adult-income DATA CLEANING AND PREPROCESSING</br>
   </br>**Kaggle Dataset**
 
  
**About The Dataset**</br></br>
An individual’s annual income results from various factors. Intuitively, it is influenced by the individual’s education level, age, gender, occupation, and etc.</br>
This is a widely cited KNN dataset.It is a good starter example for data pre-processing and machine learning practices.</br>
The dataset contains 15 columns.</br>
Target filed: Income</br>
-- The income is divide into two classes: <=50K and >50K. </br>
Number of attributes: 14.</br>
-- These are the demographics and other features to describe a person</br>
We can explore the possibility in predicting income level based on the individual’s personal information.</br></br>
**Acknowledgements**</br></br>
This dataset named “adult” is found in the UCI machine learning repository</br>
http://www.cs.toronto.edu/~delve/data/adult/desc.html</br>
The detailed description on the dataset can be found in the original UCI documentation</br>
http://www.cs.toronto.edu/~delve/data/adult/adultDetail.html</br>
 Kaggle dataset Adult income dataset (kaggle.com). </br></br>
**Get started with data:** </br>
Data Cleaning:</br>
1.	There are 15 columns and 48842 rows.</br>
2.	Checking the data types for all columns and making sure all has the right data type. </br>
3.	Removing duplicate rows (52) rows, then we will have 48790 rows.</br>
4.	Removing values of “?” in workclass, occupation and native-country” removing null values 2795 **missing values**. this will end with 45222 rows.</br>
5.	Checking education and education-num, they are similar; “If you sort ascending it will be obvious”, so here we need to delete one of them one is string and the other is numeric in this case we remove education-num, we end up with only 14 columns now.</br>
6.	Checking capital-loss and capital-gain we find out that both columns have 94% of values are 0 in both, this can be shown using column profile in view tap.</br>
7.	After checking we need to delete both columns since no point of keeping them, now we have 12 columns.</br>
8.	 Replace Never-married with single and extract first word from martial-status.</br>
![1](https://github.com/NailaAbdalla/Adult-income/assets/151609042/f27cc01c-fa55-4115-980e-ae4c7385fd3b)

 **Now we are done with data cleansing and we can start working on the dataset.** </br></br>
Data analysis:</br>
1-	First look: **33973** people with income less than or equal to 50k and **11202** with income greater than 50k.</br>
Created a measure to count how many values contain <=50K and another measure for >50k.</br>
2-	Created age bins as a new column for better age representation. </br>
![3](https://github.com/NailaAbdalla/Adult-income/assets/151609042/bcd5d622-5d91-471c-a3b7-61f0e69cff4e)</br>

Created a new column for bins using nested if with length 10 years.</br></br>
![2](https://github.com/NailaAbdalla/Adult-income/assets/151609042/bfead4a0-69bf-483a-838c-18f519b3328e)

3-	According to the personal information we need to create income levels based on the income. </br>
Age, education, marital status, race, occupation etc. All these attributes influence the income so we need to figure out this impact.</br>
•	Filter income and get some calculations and understandings: 33973 people with income<=50k.</br>
![4](https://github.com/NailaAbdalla/Adult-income/assets/151609042/aefc2da9-67d5-4381-bac1-82eb27bf179b)

•	61.69% are males with 41.22 average hours per week and 38.3% are females.</br>
![6](https://github.com/NailaAbdalla/Adult-income/assets/151609042/56431f6d-3d3e-4c6e-8680-c280deb0a8dc)

According to the race white is the highest in both income category and black comes next then aisan-pac-islander.</br>
•	For income<=50k the following marital status are from the higher till the lower: Single, married, divorced, separated, widowed. For income>50k: Married, single, divorced widowed and separated.</br>
•	According to the workclass for both income categories from highest till lowest: private, self-emp-not-inc, local-gov but other workclass has significant variations.</br>
•	According to occupation top 5 for income <=50k ascendingly, adm-clerical, craft-repair,sales,prof-specialty and exec-managers however, for income>50k exec-manag,prof-specialty,sales,craft-repair and adm-clerical.</br>
•	According to countries united states has the highest income in both income categories. </br>

predicting income level based on the individual’s personal information. this can be done by using some rules to predict income level according to our preprocessing results above or by Machine Learning.</br>
**The below report is from the dataset after cleaning process.** </br>
![7](https://github.com/NailaAbdalla/Adult-income/assets/151609042/87b80ec1-e6ba-4b3c-ab47-cda6aad42eb7)




