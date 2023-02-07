
# Set up postgres 
## 1. set up with sqlalchemy 
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
sqlalchemy.create_engine(postgresql://scott:tiger@localhost/mydatabase)

@load_ext sql
@sql postgresql://scott:tiger@localhost/mydatabase
```
