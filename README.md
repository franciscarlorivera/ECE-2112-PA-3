# ECE-2112-PA-3
Rivera, Francis Carlo E. | 2ECE-D

The repository covers Programming Assignment 3 for our ECE2112: Advanced Computer Programming and Algorithms course. The repository is divided into three programming problems that utilize slicing and indexing tools from Pandas the obtain desired data selections from a given data frame.

## INTENDED LEARNING OUTCOMES
1. Load a CSV dataset into a Pandas DataFrame
2. Select rows and columns using positional and label-based indexing
3. Filter records using conditions on a DataFrame column
4. Extract a well-defined subset of data without changing the source data

# A. POSITIONAL AND LABEL-BASED SLICING
> Objectives:
> - Load the **"cars.csv:** dataset into a Pandas data frame.
> - Display the shape and complete list of column names of cars.
> - Using positional slicing, create **"cars_6 to_10"** containing rows 6 through 10 of the dataset, where the first data row is row 1.
> - From cars 6_to_10, display only the columns **Model**, **mpg**, **cyl**, **hp**, and **gear**, in that order.

The following commands and operations were used in obtaining the required data selections from the data frame:
- `import pandas as pd` ---> Imports the Pandas library that gives access to positional indexing and slicing tools for manipulation of given data frames. The code also converts the library name to the convention pd.
- `cars = pd.read_csv('cars.csv')` ---> Reads the csv dataset and converts it into a structured Pandas data frame assigned to the named convention cars.
- `**print ('Shape of Data Frame:', cars.shape, '\n')**` ---> Displays the shape of the cars data frame next to the text "Shape of Data Frame:" and creates a line break below to separate the output from subsequent outputs.
- `cars.columns` ---> Displays the names of column headers within the cars data frame.
- `cars_6_to_10 = cars.iloc[5:10]` ---> Positional slicing command that obtains the rows 6 to 10







### VERSION HISTORY
- September 5, 2026: README File created
- September 5, 2026:
- September 5, 2026
