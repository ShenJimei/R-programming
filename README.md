# R language learning and experiment
## Experiment one 
### 1.1 Basic data structure exercise requirements:
(1) Create a vector with a value from 1 to 10, an interval of 2, and a name of A

(2) Write the numbers 1 to 12 three times each into vector B: (1,1,1, ..., 12,12,12) prompt the rep function

(3) Output the length of the B vector and the vector value after deduplication

(4) Output the intersection of A, B, union C, difference

(5) Sort set C in descending order

(6) Select the third element of C; the fourth to the last element; the element whose value is greater than or equal to 3 and less than 7

(7) Convert the numeric vector C to a character

(8) Length, maximum value and index of vector C

(9) Convert A into an array type variable named a, check the type of a

(10) Use the numbers from 1-20 to form two 4 × 5 matrices, where M1 is input by column, M2 is input by row, calculate M3 as M1 + M2; and build M4, which consists of M3 columns, but Does not include column 3

(11) Use a number from 1-9 to form a 3 × 3 matrix input by column M5; find the diagonal matrix M6 of M5

(12) Calculate the matrix multiplication of M5 and M6 to obtain M7; find the transposed matrix M8 of M7 (12) use a number from 1 to 12 to form a 4 × 3 matrix input by column M9, find the column sum of M9; Row average of M9

### 1.2 Data import and processing object Common function practice requirements:
(1) Read the algae dataset from the csv file and assign it to algae1

(2) View the first 10 data of algae1

(3) Output basic statistical information of algae1, data dimensions, feature names, and view the data types of season, size, and NO3 columns

(4) Newalgael is selected for the sample whose season is summer, and the number of newalgael sample rows is output

(5) Fill the missing value in column cl of newalgael with the median of this column

(6) Delete algae1 for samples with missing values, and output the number of rows in the original sample and the number of rows in the remaining samples

(7) Edit algae1 and save it as algae2 (arbitrarily modify the value of a point)

(8) Combine algae1 and algae2 by line to get algae3, and output the number of sample rows of algae1, algae2, and algae3

## Experiment two
### 2.1 Practice Requirements:
(1) Read item_feature1.csv into df; and name the columns of df as: date, item_id, cate_id, cate_level_id, brand_id, supplier_id, pv_ipv, cart_uv, collect_uv, and cart_ipv. Note: [date, product id, warehouse id, warehouse level id, brand id, supplier id, number of visits, purchases, collectors and purchases]

(2) Re-encode cart_uv in df and name the new variable recode, classify less than 5000 as less, classify 5000 or more and less than 15000 as common, and others as many; check the last 10 data

(3) Check whether there are missing values in df; if there are missing values, delete all rows with missing values in df

(4) Convert the date field in df to a date type, such as: 2015-02-13

(5) Sort df in ascending order of the date field and save it as df_asc; and view the first 10 data

(6) Sort df in ascending order of date field and descending order of item_id, and save it in df1; and view the first 5 data
### 2.2 Practice Requirements:
(1) Select the date, item_id, cate_id, cart_uv, recode, collect_uv, and cart_ipv fields from df and save as df1; remove the cart_ipv field from df1 and save as df2; select from df1 and save the data with item_id greater than 500 and recode as less For df3

(2) Select df as 2015-02-14, item_id as 300, and save all columns between date and supplier_id, and save as df_sub

(3) 500 samples are randomly drawn from df without replacement and saved as df4; check the dimensions of the samples and the head data of the data

(4) Select the data from item_id to cate_id from df1, save it as df1_temp, and merge with df according to item_id and save it as df5.
(5) Use sql method from df1 to select data with item_id of 300 and save it as df6. [Note: sqldf package]

(6) Randomly retrieve as many data items as df6 from df2 as df_tem, then merge with df6 in columns (horizontal) and save as df7

(7) Select date, item_id, cate_id and cart_ipv from df and save as feature, and arrange the features in ascending order by date, and take out the only cate_id in the feature

## Experiment three
### 3.1 Practice Requirements:
(1) Obtain the data by reading the file death rate.csv and save it to df. Simply analyze the data to obtain how many pieces of data are there, and whether there are missing values ​​or outliers. If there is such data, remove these data; for death Probably, its value range is 0 <q <= 1. [Note: The mortality in Questions 1-6, only consider male mortality]

(2) Draw a scatter plot to show the relationship between age, year and male mortality (logarithm is log)

(3) Draw a scatter plot of age and logarithmic survival, and analyze the relationship between the two quantities

(4) Draw a histogram to observe the distribution of male deaths

(5) Draw a histogram of the number of male logarithmic deaths (Log of Male_death) to observe the distribution of male logarithmic deaths

(6) Calculate the correlation coefficient of each variable of df and draw the correlation diagram. [With corrgram package]

### 3.2 Practice Requirements:
(1) Get the data by reading the file House-handle.csv and save it to houseIndex

(2) Data exploration, draw a chart to show the change of HPI from 1990 to 2011. The horizontal axis is time (may be the first column of the data), and the vertical axis is the HPI value

(3) Draw a graph showing the increase in HPI for each month, expressed as delta, and add a reference line at the position of 0. [Note: The amount of increase can be calculated by subtracting the next one from the previous one; the HPI value of the first one from the previous one can be considered as 1]

(4) In order to further understand the fluctuation of HPI, calculate its monthly growth rate. When plotting, months with a positive growth rate are represented by a plus sign ("+") and negative ones ("o")

(5) Establish a table for the growth rate of HPI, where each row represents a month and each column represents a year, showing the data of the previous four years (HPI growth rate is rounded to four decimal places); and an average annual growth rate of HPI is plotted Rate and average monthly growth rate of HPI (annual growth rate (column average) and monthly growth rate (row average) for all years)

(6) Draw a box chart to see the distribution of the growth rate of HPI

## Experiment four
### 4.1 Question One Requirements
(1) Save the data to df by reading “hospital-data.csv” to get the number of the data; check the first 5 data in the data

(2) View the data overview; find the range of postal codes

(3) Our default phone number is a numerical value, which has no practical meaning. The sapply function is used to return the maximum, minimum, mean, median, standard deviation, and variance of the phone number by calling a user-defined function

(4) Use aggregate to find the median of telephone numbers in each state

(5) Use by to find the maximum and minimum values of the phone numbers in each city; display the first three data of the results

(6) Generate a simple frequency table for the state; and convert this frequency table into a proportional value

(7) Establish a two-dimensional contingency table of the state and hospital type, and name it mycontable; generate marginal sums by column

(8) Use CrossTable to establish a two-dimensional contingency table of the townships to which they belong and whether or not to provide emergency services, named mycrosstable. (Note: Install the gmodels package)

### 4.2 Question Two Requirements
(1) The data obtained by reading the file death rate.csv is stored in the death, and the chi-square test is used to test whether the age is independent of the male survival population (second-level contingency table)

(2) Measure the correlation between age and male mortality (secondary contingency table) through the assocstats function

(3) Calculate the Pearson and Spearman correlation coefficients between age and male mortality; and the covariance of all variables in death

(4) Test the significance of the correlation between the female surviving population and the male surviving population

## Experiment five
### 5.1 Question One Requirements
Data processing [only use SY-20150401.csv] statistics of inbound and outbound traffic of each station every 5 minutes (Note: 00:00:01 in the first 5 minutes, 00:10:13 in the third 5 minutes ), Because you may take the subway multiple times a day, according to the card number and the arrival time, query the time of the most recent departure as the current departure time. See the functions lubridate :: hms and lubridate :: period_to_seconds.

The final result of the processing: dataframe (name trade.metro.in.out)

### 5.2 Question 2 Requirements
Use the dataframe (trade.metro.in.out) in question 1 to make statistics, and count the traffic between inbound and outbound; then select the top 10 sites with the largest traffic and view the top 6 in Notebook.
