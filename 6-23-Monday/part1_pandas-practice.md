# Monday, 6/23/25

## Part 1: Pandas review

Code from class:

```
# import pandas
import pandas as pd

# read csv
df = pd.read_csv("Iris.csv")

# display top of csv
df.head()

# provide summaries of numeric columns
df.describe()

# provide summaries of all columns
df.describe(include="all")

# summarize data with row counts, column counts, and column types
df.info()

# select a column
df["SepalLengthCm"]

# find the number of times each value appears in a column
df["Species"].value_counts()

# find the mean of a column
df["SepalLengthCm"].mean()

# find the standard deviation of a column
df["PetalWidthCm"].std()
```

Do the following with the survey data:

1. Load pandas library
1. Load the survey data
1. Display the first few rows of the survey data
1. Describe the survey data using `describe()` and `info()`
1. How many rows are in the survey data?
1. How many columns are in the survey data?
1. What is the variable type of each column?
1. Select one of the columns of the dataframe
1. Use `value_counts()` on every column
1. Find the mean of one of the columns
1. Find the standard deviation of one of the columns
1. What is something interesting you learned about the class from this data?
