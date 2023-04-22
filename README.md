![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

Welcome zemaciel,

This is the Code Institute student template for Gitpod. We have preinstalled all of the tools you need to get started. It's perfectly ok to use this template as the basis for your project submissions.

You can safely delete this README.md file, or change it for your own project. Please do read it at least once, though! It contains some important information about Gitpod and the extensions we use. Some of this information has been updated since the video content was created. The last update to this file was: **September 1, 2021**

# Database Management

!(https://gitpod.io/static/media/gitpod.a7ab6752.svg)[https://gitpod.io/static/media/gitpod.a7ab6752.svg]
Use GitPod

## **What is PostgreSQL?**

**What is it?**
A free, open source relational database management system.
**What does it do?**
Postgres has powerful features and acts as a primary database for many web and mobile applications.
**How do you use it?**
The Postgres server runs as a service on most operating systems, and can be used from the command line, through graphical clients, or directly from your own applications.

# Important!

## Error fix due to Gitpod change

**If you get the following error after typing `psql` in the terminal:**

**`psql: error: could not connect to server: No such file or directory`**

**Please use the following command in the terminal to set an environment variable needed for it to work:**

**`set_pg`**

**And then try the `psql` command again**

**You will need to do this each time you return to your Gitpod workspace for the Database Management Systems videos.**

## **PostgreSQL**

If you recall from our previous lessons, when working with data, you can choose between
relational and non-relational databases.
However, going a bit deeper into **relational databases**, Postgres is an object-relational
database, whereas MySQL is purely a standard relational database.

### **PostgreSQL**

- Object Relational Database
- Case-sensitive
- Natively supports multiple programming languages, including Python and JavaScript

### MySQL

- Standard Relational Database
- Not case-sensitive
- Limited support with other programming languages

## The learning outcomes for the following lessons will include:

- Learning how to use Postgres in its native form through the command-line interface.
- Using helpful Python adapters to perform those same queries.
- And finally, how to execute our queries programmatically from within our Python files.
- End of transcript. Skip to the start.

## Installing the Chinook database

What is it?
A series of SQL commands in a text file.
What does it do?
Allows us to script database operations, such as creating, populating, and updating databases.
How do you use it?
Put database commands in a .sql file, and run them using the Postgres command line interface.

**Extra Links:**

[Code Institute Gitpod Template](https://github.com/code-institute-org/gitpod-full-template) (**Important:** You must use this Gitpod Template to complete this module)[Chinook Database SQL](https://github.com/lerocha/chinook-database/blob/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql)

```
wget https://raw.githubusercontent.com/lerocha/chinook-database/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql
```

[Source Code Repo](https://github.com/Code-Institute-Solutions/postgresql-and-python/tree/main/01_installing_the_chinook_database)

[****COMMANDS.md****](https://www.notion.so/COMMANDS-md-bd786dbd3e094c929407268a570699c4)

1. Create a new repository and used the following code on the terminal to get the sample data base:  `wget https://raw.githubusercontent.com/lerocha/chinook-database/master/ChinookDatabase/DataSources/Chinook_PostgreSql.sql`
2. A new file called `Chinook_PostgreSql.sql` is created.
3. Next, we need to start the Postgres command-line interface, or shell, in order to get the Chinook database installed, and the data populated. To launch the Postgres CLI, we can simply type "`psql`" and hit enter.
4. To view, or list any database in our enviromenment type `\l`  (backslash+L)
    
    ![Screenshot 2023-04-22 at 09.39.21.png](readme/01deafult_databases.png)
    
5. By default PostgreSQL has three databases out-of-the-box:
`postgres
template0
template1`
6. **Create a new database** Instead of using any of these default databases, let's create a new database for our Chinook lessons. `CREATE DATABASE chinook;` **Don't forget the semicolon at the end of the command.**
7. To change between databases use `\c databasename`
example: `\c postgres` 
`\c chinook`
8. The `\c` (*backslash C stands)* for **connect**, telling to which database you want to connect. 
9. Finally, while we're connected to our new chinook database, we need to **initialise** or
**install** the downloaded sample Chinook PostgreSQL database.
Type: `\i Chinook_PostgreSql.sql`  (CASE SENSITIVE!)
The `\i` generally means include, integrate, **install, or initialise**.
*Essentially, this file is an SQL script that contains all of the instructions needed to
create tables, and populate our database with information so that we have useful data for practice.*
10.