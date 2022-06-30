# Movies-ETL
Extract, Transform, Load

## Purpose
1. Create an ETL pipeline from raw data to a SQL database.
2. Extract data from disparate sources using Python.
3. Clean and transform data using Pandas.
4. Use regular expressions (Regex) to parse data and to transform text into numbers.
5. Load data with PostgreSQL and verify in PgAdmin.

The project included extracting a large data set from Kaggle, then transforming the data into a usable dataset for a "hacking competition."  Once the data was transformed and narrowed in scope for the hack-a-thon, the DataFrames were loaded into PostgresSQL.  

## Extracting
Wikipedia Movies JSON file, starting with 193 Columns:
<img width="1079" alt="Screen Shot 2022-06-29 at 9 03 25 PM" src="https://user-images.githubusercontent.com/104115586/176584948-06f0fc8a-605a-42d4-ab3a-90734cc3bffd.png">


Kaggle Movie Metadata, 24 columns
<img width="1097" alt="Screen Shot 2022-06-29 at 9 03 41 PM" src="https://user-images.githubusercontent.com/104115586/176584960-d82d9e9c-f86e-4290-a649-f31e68541118.png">


Kaggle Ratings data, 2602489 rows by 4 columns

<img width="402" alt="Screen Shot 2022-06-29 at 9 04 29 PM" src="https://user-images.githubusercontent.com/104115586/176584978-08877e47-e48c-44de-8866-dfd655457c7c.png">



## Transforming 
### Wikipedia Data
Wikipedia Movies transformed, 22 columns
<img width="1093" alt="Screen Shot 2022-06-29 at 9 04 44 PM" src="https://user-images.githubusercontent.com/104115586/176584999-53406b5d-7a4e-4665-910d-563c0ec785a9.png">


Wikipedia Movies, making the column names more succinct and uniform, 7033 rows of data.
<img width="712" alt="Screen Shot 2022-06-29 at 9 05 20 PM" src="https://user-images.githubusercontent.com/104115586/176585016-3f4f8ba3-841b-4d0b-a9e7-6128edd11d4e.png">

### Kaggle Data
Wikipedia Movies merged with Kaggle Movies data, all column names and row counts, 6052 rows.
<img width="1107" alt="Screen Shot 2022-06-29 at 9 07 07 PM" src="https://user-images.githubusercontent.com/104115586/176585037-4c3413ac-8674-4acf-af3c-f208ba8f1b59.png">

Merged Movies with Kaggle ratings, all of the column names and row counts, 6052 rows.
<img width="422" alt="Screen Shot 2022-06-29 at 9 07 44 PM" src="https://user-images.githubusercontent.com/104115586/176585051-dcd7cc66-8192-4070-97b3-693a7ffe3236.png">



## Loading
### Creating the Movie Database
Sending the data to PostgresSQL
<img width="832" alt="Screen Shot 2022-06-29 at 9 08 04 PM" src="https://user-images.githubusercontent.com/104115586/176585074-85bc5773-4872-4624-a8ef-f98546721626.png">


### Verifying the data in PgAdmin
Movies Query

![Screen Shot 2022-06-29 at 9 08 26 PM](https://user-images.githubusercontent.com/104115586/176585086-481fad21-0ddc-4431-b989-ddaf4fff91ec.png)


Ratings Query

![Screen Shot 2022-06-29 at 9 08 36 PM](https://user-images.githubusercontent.com/104115586/176585103-928d5af8-5291-4db3-89bd-edcf5c4fda74.png)


## Summary

A JSON file and 2 Kaggle files were extracted, then transformed, and joined.  A movies and ratings file were loaded into a database for the hack-a-thon event.
