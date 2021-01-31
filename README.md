## Data modeling with Postgres
### Summary
Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables.

* Fact Table:
 - songplays: songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
* Dimension Tables: 
 - users: user_id, first_name, last_name, gender, level
 - songs: song_id, title, artist_id, year, duration
 - artists: artist_id, name, location, latitude, longitude
 - time: start_time, hour, day, week, month, year, weekday

Star schemas are denormalized, meaning the typical rules of normalization applied to transactional relational databases are relaxed during star-schema design and implementation. The benefits of star-schema denormalization are:

* Simpler queries
* Query performance
* Fast aggregations

The project includes six files:

* test.ipynb displays the first few rows of each table to let you check your database.
* create_tables.py drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.
* etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.
* etl.py reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.
* sql_queries.py contains all your sql queries, and is imported into the last three files above.
README.md provides discussion on your project.

### Build ETL Pipeline
Run create_tables.py to create/reset your tables. Run etl.py to process the entire datasets  Run test. Finally run test.ipynb to confirm your records were successfully inserted into each table.