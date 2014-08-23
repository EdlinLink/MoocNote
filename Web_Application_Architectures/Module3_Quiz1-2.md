## Question 1

In a relational database, a row in a table corresponds to what?

+ A record
+ An attribute

> 参考PPT M3-L1-RelationalDBs-Handout - Relational Databases.

## Question 2

In a relational database, a column in a table corresponds to what?

+ An attribute
+ A record

> 参考PPT M3-L1-RelationalDBs-Handout - Relational Databases.

## Question 3

The acronym SQL stands for what?

> 参考PPT M3-L1-RelationalDBs-Handout - Relational Databases.

## Question 4

In a relational database, the field that points to the primary key of another record is called what?

> 参考PPT M3-L1-RelationalDBs-Handout - Relational Databases.

## Question 5

SQlite is suitable for production environments.

True
False

> 参考PPT M3-L2-RailsDBs-Handout - Rails Databases. Rails automatically sets up the development environment to use SQLite, a simple easy-to-use file-based relational database that runs in memory. When an application goes into production, it may receive 100’s or 1000’s of “hits” in a matter of seconds, and the database needs be able to handle the data requests associated with these hits.

## Question 6

What file within a Rails application is used to construct the database?

+ schema.rb
+ migration files
+ database.yml

> Each time we ran the scaffold generator in our blog application, Rails created a database migration file and placed it in the db/migrate directory. Rails uses the rake command to run these migrations, which creates a schema, from which appropriate databases can then be created;
> The databases that Rails will use in different environments is specified in: db/database.yml.
