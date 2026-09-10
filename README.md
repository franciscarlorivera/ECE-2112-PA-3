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
> - The row selection in part (b) must use iloc; the column selection in part (c) must use column labels.

The following commands and operations were used in obtaining the required data selections from the data frame:
- `import pandas as pd` ---> Imports the Pandas library that gives access to positional indexing and slicing tools for manipulation of given data frames. The code also converts the library name to the convention pd.
- `cars = pd.read_csv('cars.csv')` ---> Reads the csv dataset and converts it into a structured Pandas data frame assigned to the named convention cars.
- `cars` ---> Calls out the data frame stored in cars derived from the cars.csv dataset.
- `print ('Shape of Data Frame:', cars.shape, '\n')` ---> Displays the shape of the cars data frame next to the text "Shape of Data Frame:" and creates a line break below to separate the output from subsequent outputs.
- `cars.columns` ---> Displays the names of column headers within the cars data frame.
- `cars_6_to_10 = cars.iloc[5:10]` ---> Positional slicing command that obtains the 6th to 10th row of the cars data frame with respect to their row indices. The selected rows are stored in cars_6_to_10.
- `cars_6_to_10.loc[:,['Model', 'mpg', 'cyl', 'hp', 'gear']]` ---> Filters the data columns of the selected rows and only retains the data stored within the chosen columns: 'Model', 'mpg', 'cyl', 'hp', and 'gear'. The command displays the resulting modified data frame.

```
import pandas as pd

cars = pd.read_csv('cars.csv')
cars

print ('Shape of Data Frame:', cars.shape, '\n')
cars.columns

cars_6_to_10 = cars.iloc[5:10]
cars_6_to_10.loc[:,['Model', 'mpg', 'cyl', 'hp', 'gear']]
```

# B. MODEL LOOKUP
> Objectives:
> - Use Boolean indexing on the Model column to obtained the required data selections
> - Display the complete row for Toyota Corolla.
> - For Pontiac Firebird, display only Model, mpg, hp, and wt.
> - Store the two results in toyota and pontiac, respectively. Do not use a hard-coded row number to locate either model.

The following commands and operations were used in obtaining the required data selections from the data frame:
- `toyota = cars.loc[cars['Model']== 'Toyota Corolla']` ---> Filters the cars data frame using a Boolean condition that works through the data listed under the Model data column until the desired data, Toyota Corolla, is located. The row that matches the required criteria is then stored in the named convention 'toyota'
- `toyota` ---> Calls out the filtered data frame stored in toyota.
- `pontiac = cars.loc[cars['Model']== 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]` ---> Filters the cars data frame using a Boolean condition that locates the data, Pontiac Firebird, under the Model data column. The command then filters the data columns and only retains the data under the selected columns: 'Model', 'mpg', 'hp' and 'wt'. The filtered data frame is stored under the named convention 'pontiac'.
- `pontiac` ---> Calls out the filtered data frame stored in pontiac.

```
toyota = cars.loc[cars['Model']== 'Toyota Corolla']
toyota

pontiac = cars.loc[cars['Model']== 'Pontiac Firebird', ['Model', 'mpg', 'hp', 'wt']]
pontiac
```

# C. MULTI-MODEL SUBSETTING
> Objectives: 
> - Create a DataFrame named selected cars containing only the records for three models: Datsun 710, Lotus Europa, and Ferrari Dino.
> - For these records, retain only Model, mpg, cyl, hp, and gear.
> - Select the rows by their model values rather than by row numbers.
> - Display selected cars and its shape.
> - The final DataFrame must contain exactly three rows and five columns.

The following commands and operations were used in obtaining the required data selections from the data frame:
- `target = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']` ---> Creates a list assigned to the variable named 'target' that contains three specified strings: 'Datsun 710', 'Lotus Europa', and 'Ferrari Dino'.
- `selected_cars = cars.loc[cars['Model'].isin(target), ['Model', 'mpg', 'cyl', 'hp', 'gear']]` ---> Filters the cars data frame using a Boolean condition that locates the three specified data located in the variable named target under the Model data column. The command filters the data frame further by retaining the data under the specified data columns: 'Model', 'mpg', 'cyl', 'hp', and 'gear'. The modified data frame is stored in the named convention selected_cars.
- `selected_cars` ---> Calls out the modified data frame stored in selected_cars.
- `print ('Shape of Data Frame:', selected_cars.shape)` ---> Displays the shape of the selected_cars data frame next to the text "Shape of Data Frame:".

```
target = ['Datsun 710', 'Lotus Europa', 'Ferrari Dino']
selected_cars = cars.loc[cars['Model'].isin(target), ['Model', 'mpg', 'cyl', 'hp', 'gear']]
selected_cars

print ('Shape of Data Frame:', selected_cars.shape)
``` 

### VERSION HISTORY
- September 5, 2026: README File created.
- September 5, 2026: Added content for introductory section.
- September 5, 2026: Completed content for Part A and Part B.
- September 5, 2026: Completed contet for Part C.
- September 7, 2026: Uploaded Jupyter Notebook File.
- September 10, 2026: Uploaded revised Jupyter Notebook File
- September 10, 2026: Updated content for Part A.
- September 10, 2026: Uploaded cars.csv file.
