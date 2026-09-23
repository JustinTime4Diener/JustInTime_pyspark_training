# PySpark Beginner Course Outline
### Author: Justin Diener

## Course outcome

To teach the basics of pyspark and is covered in 10 notebooks each standalone.  Notebook 10 requires Fabric or similar with the NYC yellow taxi sample dataset.  Hope you enjoy.

## 01 - Why Spark and Working in Fabric

- Run cells in a Fabric notebook
- Driver, executors, tasks, and partitions
- Transformations, actions, and lazy evaluation
- Shuffles, caching, lineage, and safe use of `collect()`
- **Exercise:** identify the execution trigger and risky data movement

## 02 - DataFrames and Schemas

- Create a DataFrame with a DDL schema string
- Preview with `show()`
- Inspect with `printSchema()`, `columns`, and `dtypes`
- Select and alias columns
- DataFrame immutability
- **Exercise:** build a renamed product-price projection

## 03 - Filtering and Creating Columns

- `F.col` and `F.lit`
- `filter`, `isin`, and parenthesised boolean expressions
- **Exercise**: try filtering yourself
- Calculated columns with `withColumn`
- Conditional columns with `when` / `otherwise`
- `select`, `withColumnRenamed`, `drop`, and `orderBy`
- **Exercise:** create a sorted high-value order report

## 04 - Data Types, Casting, and Bad Records

- Common scalar Spark types (i.e. one atomic value)
- `cast` for trusted input
- `try_cast` for uncertain input
- Preserve raw values and flag conversion failures
- Schema-on-read versus cleanup after read
- **Exercise:** type and validate a raw product extract

## 05 - Missing and Duplicate Data

- Null versus blank text
- Basic text standardisation with `trim`
- `isNull` and `isNotNull`
- `coalesce`, `fillna`, and `dropna`
- Exact duplicates and the limits of `dropDuplicates(keys)`
- A simple data-quality count
- **Exercise:** build a repeatable customer-cleaning pipeline

## 06 - Grouping and Aggregations

- Input and output grain
- `groupBy` and `agg`
- `sum`, `avg`, `min`, `max`, and `countDistinct`
- `count('*')` versus `count(column)`
- Multiple grouping keys and sorted results
- Temporary views and an equivalent Spark SQL query
- **Exercise:** create a category performance summary

## 07 - Joining and Combining DataFrames

- Inner and left joins
- DataFrame aliases and qualified columns
- Join cardinality and row-count validation
- Right, full, semi, and anti join reference
- Find unmatched records with a left-anti join
- Append compatible rows with `unionByName`
- **Exercise:** retain every order while assigning customers and account managers

## 08 - Dates and Timestamps

- Parse with explicit formats and `try_to_timestamp`
- Detect invalid dates and timestamps
- Extract year, month, day, and day of year
- `date_format` for display labels
- `datediff`, `date_add`, and timestamp intervals
- Named time-zone conversion
- **Exercise:** parse day-first delivery data and create calendar fields

## 09 - Window Functions and Pipeline Recap

- `Window.partitionBy` and `orderBy`
- `row_number` within a business key
- Deterministic latest-record selection
- End-to-end afternoon pipeline checklist
- **Exercise:** choose the latest product price

## 10 - Reading and Writing in Microsoft Fabric

- Attach a default Lakehouse
- Use `Files/pyspark_training` paths
- Read CSV with an explicit schema
- Path-based Delta data versus managed Delta tables
- `overwrite`, `append`, `error`, and `ignore` modes
- `save`, `saveAsTable`, `load`, and `spark.table`
- **Exercise:** create and verify `retail_customers`

## Function-to-notebook index

| Need | Main APIs | Notebook |
|---|---|---:|
| Inspect data | `show`, `printSchema`, `columns`, `dtypes` | 02 |
| Choose columns | `select`, `alias` | 02, 03 |
| Convert types | `cast`, `try_cast` | 04 |
| Filter rows | `filter`, `isin`, `isNull` | 03, 05 |
| Create or remove columns | `withColumn`, `F.lit`, `drop`, `withColumnRenamed` | 03 |
| Apply business conditions | `when`, `otherwise` | 03 |
| Handle missing data | `coalesce`, `fillna`, `dropna` | 05 |
| Clean text and duplicates | `trim`, `dropDuplicates` | 05 |
| Summarise groups | `groupBy`, `agg`, aggregate functions | 06 |
| Use Spark SQL | `createOrReplaceTempView`, `spark.sql` | 06 |
| Combine datasets | `join`, `unionByName` | 07 |
| Work with dates | `try_to_timestamp`, date functions, time zones | 08 |
| Read and write Lakehouse data | `spark.read`, `save`, `saveAsTable`, `spark.table` | 10 |
| Choose a latest record | `Window`, `row_number` | 09 |

## Optional topics if time permits

1. Delta `MERGE`, schema evolution, and table history
2. `rank`, `lag`, `lead`, and running window calculations
3. Broadcast joins, partition control, caching, data skew, and Spark UI
4. Nested JSON, arrays, structs, `from_json`, and `explode`
5. Regex and deeper string standardisation
6. Structured Streaming and incremental ingestion
7. Transformation tests, data-quality expectations, parameters, and orchestration

RDDs, MLlib, custom UDF development, streaming implementation, and advanced cluster tuning are outside the mandatory beginner path.
