# Embedded_SQL_BASIC
Database Assignment done using Python in Jupyter Notebook to implement SQL commands

Here is an assignment that I recently completed where I was to add assertions and triggers
to my PostgreSQL16 database that I had created in a previous assignment. For this assignment,
we were given the task of doing the final question via EmbeddedSQL, in otherwords, using another
programming language of our choice to implement the SQL commands. I decided to take it a step
further and create the entire database, add the tables, update the primary key columns,
and add the data as well, all without actually using the PostgreSQL16 database.  I created functions to 
create the database after checking to see whether it exists already, create tables, add columns to the 
tables, view the tables, and remove rows from the table after the table's creation. 
After creating these functions and recreating the tables used in the assignment, 
I added constraint triggers to the databases, again, using only embeddedSQL to do so.

LIMITATIONS TO NOTE: 

The functions for creating tables, adding columns and removing rows are extremely basic.
The row removal function **remove_rows_from_table()** works fine for this assignment, due to the small number of rows, 
so I've implemented it to remove rows by row number, rather than by condition. 
However, any larger database that one would typically see would not want to use this generally, 
unless there were a way that the condition would end up choosing the row number in
the way that I've set it up. 

The column adding function **add_column()** only uses three datatypes, as were needed in this assignment, which are 
varchar(n), numeric(p,s) and int. The function could easily be expanded to other datatypes, but here, there were only 3 needed.

The main purpose of this is to show some basic usage of EmbeddedSQL and also to illustrate the usage of some more moderately
complex SQL statements and how they can still be used in this context, as my online searches for examples to help me complete the assignment
mostly showed smaller basic two line SQL statements. 

ADDED NOTE REGARDING PORT 5434

For connecting to my database, I used port 5434, rather than the standard port 5432, due to having to reinstall PostgreSQL and
needing to use a different location
