# Data-Science


Data cleaning():
In this function, df is the input dataframe. The function performs the following steps:

Creates a new column "inc/dec percentage" by subtracting the values in "Level 4" from those in "Level 1" and dividing the result by "Level 1".
Replaces any missing values (null values) in the dataframe with the mean of each respective column.
Replaces the abbreviations for months in column 'B' with their full names using the apply method and a lambda function.
Replaces the values in column 'E' with "From LinkedIn" for "Came_From_LinkedIn" and "Direct_traffic" for "Landed_Directly".



Descriptive_stats:
In this function, df is the input dataframe and the other parameters are the filters for the year, month, device, customer type, and source. The function performs the following steps:

Finds the minimum value among all level columns (Level 1, 2, 3, 4) using the min method twice.
Finds the maximum value of the ratio of Level 2 divided by Level 1 among customers who came directly via desktop website. This is done by filtering the dataframe to only include those rows that meet the conditions, then using the apply method and a lambda function to calculate the ratios, and finally using the max method to find the maximum.
Filters the dataframe based on the given parameters (or their default values).
Generates summary statistics (mean, median, quartiles, standard deviation) for all numerical columns in the filtered dataframe. This is done by finding the numerical columns using the _get_numeric_data method and calling the describe method on the resulting dataframe.
Finds the unique values and data types for all non-numeric columns in the filtered dataframe. This is done by using the columns.difference method to find the non-numeric columns and then looping through them to print the unique values



