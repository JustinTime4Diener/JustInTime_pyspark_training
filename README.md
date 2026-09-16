# PySpark for Beginner Data Engineers

This repository contains a three-hour, Microsoft Fabric-first introduction to PySpark followed by a separate three-hour practical problem.

The ten student notebooks build from Spark's execution model to an end-to-end batch pipeline. Each notebook is independently runnable and includes:

- learning objectives and a prerequisite recap;
- short demonstrations using a consistent retail scenario;
- a transferable exercise;
- an expected result and a separated solution; and
- a takeaway and pointer to the next lesson.

## Microsoft Fabric prerequisites

1. Create or open a **Spark / PySpark** notebook.
2. Attach a default Lakehouse.
3. Upload the files from `pyspark_training_interns/retail_data` to `Files/pyspark_training` in that Lakehouse.
4. Run each notebook from top to bottom.

Fabric supplies the `spark` session. The student notebooks do not stop or replace it. See Microsoft's guidance for [choosing the Fabric Spark kernel](https://learn.microsoft.com/en-us/fabric/data-engineering/fabric-notebook-selection-guide) and [reading and writing Lakehouse data](https://learn.microsoft.com/en-us/fabric/data-engineering/lakehouse-notebook-load-data).

## Morning schedule

| # | Notebook | Minutes |
|---:|---|---:|
| 01 | Why Spark and Working in Fabric | 10 |
| 02 | DataFrames and Schemas | 14 |
| 03 | Filtering and Creating Columns | 20 |
| 04 | Data Types, Casting, and Bad Records | 16 |
| 05 | Missing and Duplicate Data | 15 |
| 06 | Grouping and Aggregations | 18 |
| 07 | Joining and Combining DataFrames | 22 |
| 08 | Dates and Timestamps | 15 |
| 09 | Window Functions and Pipeline Recap | 15 |
| 10 | Reading and Writing in Microsoft Fabric | 20 |

The lessons total 165 minutes, leaving approximately 15 minutes for questions, Spark-session delays, and transitions.

## Course conventions

- Input root: `Files/pyspark_training`
- Input files: `orders.csv`, `customers.csv`, and `products.csv`
- Managed training tables: `retail_orders` and `retail_customers`
- Training writes use `overwrite` so the lesson can be rerun safely
- `append` is explained but is not the default because rerunning it can duplicate data

The local Spark helper under `_local_dev` is for repository testing only and is not part of the student path.

## Afternoon readiness

Students finish the morning able to:

1. read the three CSVs with explicit schemas;
2. inspect and validate types;
3. clean nulls, blanks, and duplicates;
4. derive order values and date features;
5. join lookup data;
6. aggregate and sort a business result; and
7. write and verify a managed Delta table.

See [Course_outline.md](pyspark_training_interns/Course_outline.md) for the detailed topic and function index.

## Optional extension topics

1. Delta `MERGE`, schema evolution, and table history
2. More window functions: `rank`, `lag`, `lead`, and running totals
3. Broadcast joins, repartitioning, caching, data skew, and the Spark UI
4. Nested JSON, arrays, structs, `from_json`, and `explode`
5. Regex-based string cleaning
6. Structured Streaming and incremental ingestion
7. Automated tests, data-quality expectations, notebook parameters, and orchestration
