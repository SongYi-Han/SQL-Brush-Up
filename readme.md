
# How to set up

reference: 
* https://www.postgresqltutorial.com/postgresql-getting-started/load-postgresql-sample-database/ : how to load data in postgres

## Set up postgres with pdAdmin locally

Most intuitive way is 
1) Install a Postgres server locally and create a database with pgAdin 
    * importand variables: `username`, `password`, `prot`, `databasename`
2) Use Python with SQLAlchemy to connect to the database, create tables, insert data and query database

### sqlalchemy 
* reference : https://towardsdatascience.com/heres-how-to-run-sql-in-jupyter-notebooks-f26eb90f3259
* requirements :  
`pyodbc` — for SQL Server  
`mysql` — for MySQL  
`psycopg2` — for PostgreSQL  

### Jupyter as SQL IDE 
```
!pip install ipython-sql

# create connection 
import sqlalchemy
sqlalchemy.create_engine(postgres+psycopg2://<USERNAME>:<PASSWORD>@<IP_ADDRESS>:<PORT>/<DATABASE_NAME>)

@load_ext sql
@sql postgresql://scott:tiger@localhost/mydatabase
```
