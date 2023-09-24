_**Created by @jl33-ai 👦🏻**_

Hello there! :wave: This step-by-step guide will provide you with a comprehensive overview of ETL processes.
ETL stands for **Extract**, **Transform** and **Load**. These are the three basic steps that are used in data warehousing for integrating data from multiple heterogeneous data sources.

## Table of contents
1. [Extraction: :outbox_tray:](#Extraction)
2. [Transformation: :arrows_clockwise:](#Transformation)
3. [Loading: :inbox_tray:](#Loading)
4. [Python Libraries for ETL :snake:](#Python Libraries)
5. [Examples](#Examples)
 
## Extraction :outbox_tray:

Extraction is the first part of the ETL process where data is extracted from the source system into the ETL environment.

- Retrieving data can be a complex process because we are dealing with a wide variety of source systems and structures.
- Examples of extraction types include full extraction, partial extraction, and incremental extraction.

## Transformation :arrows_clockwise:

This process of transformation involves enhancing the extracted data so that it can be used in a company’s data warehouse.
- There are different types of transformations, such as cleaning, filtering, merging, splitting, summarizing, and aggregating.
- Example: If we have a date field in "dd-mm-yy" format, we may want to transform it into a "yyyy-mm-dd" format.

## Loading :inbox_tray:

The final process is the loading phase where transformed and validated data is loaded into a data warehouse.

- Load process can be a full load or incremental load depending upon the requirement.
- Keep in mind that loading should not affect the performance of the data warehouse.

## Python Libraries for ETL :snake:

1. **Pandas**: Provides data manipulation and analysis capabilities.
2. **NumPy**: Deals with mathematical computation on arrays and matrices.
3. **SQLAlchemy**: A SQL toolkit that provides a full suite of well known enterprise-level persistence patterns.
4. **Petl**: A general purpose Python package for extracting, transforming and loading tables of data.
    
## Examples

1. **Extraction Example**
    ```python
    import pandas as pd
    df = pd.read_csv('/path/to/your/file.csv')
    ```

2. **Transformation Example**
    ```python
    df['date'] = pd.to_datetime(df['date'], format='%d-%m-%y')
    df['date'] = df['date'].dt.strftime('%Y-%m-%d')
    ```

3. **Loading Example**
    ```python
    from sqlalchemy import create_engine
    engine = create_engine('postgresql://username:password@localhost:5432/mydatabase')
    df.to_sql('table_name', engine)
    ```
