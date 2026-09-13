## 01 - Why Spark

1. Working in a notebook
2. Why does spark exist
3. Spark exection model
4. lazy evaluation explained
5. **Exercise**: Quick question about which operation triggers exection

## 02 - Intro to DataFrames

1. What is a dataframe
2. Creating a small standalone dataframe
3. How to preview with show()
4. How to inspect the schema of a dataframe
5. How to Select columns to return from a dataframe
6. **Exercise**: Do a select from a larger DF using only 2 columns and preview it

## 03 - Filtering and creating columns


1. Refer to columns using col()
2. Using filter() with operands
3. **Exercise**: Using operands or and Not
4. Using withColumn to calculate a new column
5. **Exercise**: Adding a new calculated column

## 04 - Conditional columns

1. Using when() and otherwise()
2. **Exercise**: creating dataframes with conditional columns using when and otherwise()

## 05 - Missing Data and Fallback Values

1. Identify missing values with isNull and isNotNull
2. Using Coalesce()
3. Using filna()
4. Using dropna()

## 06 - GroupBy and aggregations

1. single aggregation using count()
2. single aggregation using sum()
3. Multiple aggregations using agg()
4. Grouping by more than one column
5. **Execersie**: Creating aggregates

## 07 - joining dataframes

1. Inner joins
2. Left joins
3. **Execersie**: Answering a business question

## 08 - Read and Write data

1. Read CSV files using an explicit schema
2. Inspect a DataFrame schema after reading data
3. Write and read managed Delta tables
4. **Exercise**: Read and write a customer table

## 09 - Dates and Timestamps

1. Parse date and timestamp strings using explicit formats
2. Format dates and extract calendar fields
3. Calculate date differences and add time to timestamps
4. Convert UTC timestamps to a named local time zone
5. **Exercise**: Parse delivery data and create calendar features

## 10 - Spark Data Types and Casting

1. Inspect schemas and identify common Spark data types
2. Cast string values to numeric, decimal, boolean, date, and timestamp types
3. Use safe casts and identify failed conversions with null values
5. **Exercise**: Clean a raw product extract into an analysis-ready DataFrame
