<h2>Data modeling with Postgres</h2>
<h3>Summary</h3>
Using the song and log datasets, you'll need to create a star schema optimized for queries on song play analysis. This includes the following tables.

* Fact Table:songplays 
* Dimension Tables: users, songs, artists, time

Star schemas are denormalized, meaning the typical rules of normalization applied to transactional relational databases are relaxed during star-schema design and implementation. The benefits of star-schema denormalization are:

* Simpler queries
* Query performance
* Fast aggregations


<h3>Build ETL Pipeline</h3>
Run create_tables.py to create/reset your tables. Run etl.py to process the entire datasets  Run test. Finally run test.ipynb to confirm your records were successfully inserted into each table.