# Pandas

A library used for data manipulation.
Here we start with Series, What series are ? and How to create Series.

## **1. Series**

`Series is a 1D Array capable of holding any datatype and it always be vertical. Also the index number is called Labels and index both.`

**Method of Creation**
There are multiple ways of creating a series, some of them are,

- Using a List
- Using an Array
- Using a Dictionary

## **2. Data Frames**

When we combine multiple series it creates a dataframe.

`DataFrames are 2-dimensional labeled data structures in Pandas. They can be thought of as a collection of Series objects that share the same index.`

### Methods of Creation

Data Frames can be created using

- Lists
- Dictionary

Further we learned how to

1. Access a Column
2. How to access Multiple columns
3. How to remove a column
4. How to remove multiple columns
5. How to access a row

Then we explored how to do `Conditional Selection` and `Multiple Conditional Selection` in data frame.

## **Missing Data / Values**

### 1. Finding Missing Values

The first thing we've to do, is to find the missing data or values, and we can do that with the help of `isna()` function. We can also do some other thing using the following functions

```python
1. my_df.isna() #Give us True/False for missing and non missing values
2. my_df.isna().sum() #Gives us the how many null values are there in each row.
3. my_df.isna().any() #It will return whether each row has all null or data ?
```

### 2. Deleting Missing Data

We can delete the missing data using the following ways

```python
1. my_df.dropna() # This will simply drop the rows having null data
2. my_df.dropna(thresh = 3) # This will drop rows which have 3 or more non-null values
```

### 3. Filling Missing Data

We can fill the missing values with following methods

``` python
1. my_df.fillna(0) #This will fill all null values with zero
2. my_df.fillna(values) # Provide a dict (values) for storing values for null values
```

## Merging Joining and Concatination

### 1. Merging

Merging means to merge two DataFrames, having a common column (key, element). We can Merge two DataFrames using the merge function of Pandas,

```python
pd.merge(employees, salaries, on = employee_id, how = inner) # inner is the common column, key & how is the mode how to join two DataFrame
```

### 2. Concatination

Concatination is same like merging but it uses the key word `concat` as function like the following

``` python
pd.concat([df1, df2]) # [] This contain list of DataFrames
pd.concat([df1, df2], axis = 1) # Concatenate along columns
```  

### 3. Joining

Used for joining two dataframes, 

``` python
df1.join(df2) # This will join both and df1 comes first then df2 will come
df2.join(df1) # This will join both & df1 comes first then df2 will come