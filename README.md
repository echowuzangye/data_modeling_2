# data_modeling_2 with Apache Cassandra

### Datasets
For this project, you'll be working with one dataset: event_data. 

### Build ETL Pipeline
- Implement the logic in section Part I of the notebook template to iterate through each event file in event_data to process and create a new CSV file in Python
- Make necessary edits to Part II of the notebook template to include Apache Cassandra CREATE and INSERT statements to load processed records into relevant tables in your data model
- Test by running SELECT statements after running the queries on your database

### Personal notes
- Table names should reflect the query it is going to answer
- Select only the relevant columns in the select statements
- The sequence of the columns in the CREATE and INSERT statements should follow the order of the COMPOSITE PRIMARY KEY and CLUSTERING COLUMNS
CREATE TABLE IF NOT EXISTS some_table(A int, B int, C text, D float, PRIMARY KEY(A, B))
- The csv reader reads all data as text, so convert fields into appropriate data types before inserting into a table
- If there is a space after the backslash, then the error occurs. By removing the space, it works
